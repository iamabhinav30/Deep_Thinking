# JavaScript Deep Thinking

## Event Loop and Task Queues

### Why is setTimeout a macrotask?

`setTimeout` is a macrotask (also called a task) because:

1. **Browser API Origin**: `setTimeout` is a Web API provided by the browser environment (or Node.js runtime), not part of the JavaScript language itself.

2. **Execution Model**: When you call `setTimeout`, the browser schedules the callback to be executed after the specified delay. This callback is placed in the **macrotask queue** (also known as the task queue or callback queue).

3. **Priority and Timing**: Macrotasks are processed one at a time after the call stack is empty and all microtasks have been executed. Each macrotask represents a discrete unit of work that can be interrupted by microtasks.

4. **Examples of Macrotasks**:
   - `setTimeout`
   - `setInterval`
   - `setImmediate` (Node.js)
   - I/O operations
   - UI rendering
   - User interactions (click, scroll, etc.)

**Example**:
```javascript
console.log('1');
setTimeout(() => console.log('2'), 0);
console.log('3');
// Output: 1, 3, 2
```

### Why is Promise.resolve() a microtask?

`Promise.resolve()` is a microtask because:

1. **Native JavaScript Feature**: Promises are part of the ECMAScript specification and are natively supported in JavaScript. Their callbacks (`.then()`, `.catch()`, `.finally()`) are queued as microtasks.

2. **Execution Model**: When a promise is resolved, its `.then()` or `.catch()` handlers are placed in the **microtask queue** (also known as the job queue).

3. **Higher Priority**: Microtasks have higher priority than macrotasks. After each task from the call stack completes, the event loop processes **all** microtasks in the queue before moving to the next macrotask.

4. **Examples of Microtasks**:
   - `Promise.then()`, `Promise.catch()`, `Promise.finally()`
   - `async/await` (which is syntactic sugar over promises)
   - `queueMicrotask()`
   - `MutationObserver`

**Example**:
```javascript
console.log('1');
Promise.resolve().then(() => console.log('2'));
console.log('3');
// Output: 1, 3, 2
```

### Comparing Macrotasks and Microtasks

```javascript
console.log('1');

setTimeout(() => console.log('2 - setTimeout'), 0);

Promise.resolve().then(() => console.log('3 - Promise'));

console.log('4');

// Output:
// 1
// 4
// 3 - Promise
// 2 - setTimeout
```

**Explanation**:
1. `console.log('1')` - executes immediately (synchronous)
2. `setTimeout` - callback queued in macrotask queue
3. `Promise.resolve().then()` - callback queued in microtask queue
4. `console.log('4')` - executes immediately (synchronous)
5. Call stack is now empty, event loop checks microtask queue first
6. `console.log('3 - Promise')` - executes (microtask)
7. All microtasks complete, event loop moves to macrotask queue
8. `console.log('2 - setTimeout')` - executes (macrotask)

### Event Loop Processing Order

1. Execute all synchronous code in the call stack
2. Execute **ALL** microtasks in the microtask queue
3. Execute **ONE** macrotask from the macrotask queue
4. Execute **ALL** microtasks that were queued during step 3
5. Render updates (if any)
6. Repeat from step 3

This is why microtasks always execute before macrotasks, even if the macrotask was queued first.
