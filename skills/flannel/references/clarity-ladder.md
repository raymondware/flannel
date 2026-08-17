# The Clarity Ladder, worked examples

Each rung, with a before (word salad) and after (Flannel) version.

## 1. Would a first-time reader get it without a follow-up question?

**Before**: `processData(d)` — reader has to open the function to know what `d` is or what
"process" means here.

**After**: `normalizeUserEmails(emails)` — the name answers the question before it's asked.

## 2. Does the name already say the "what"?

**Before**: `x = calc(a, b, 1)` — the `1` is a mystery flag.

**After**: `total = calculateTotal(price, quantity, { roundUp: true })` — no need to read the
function body to know what's happening.

## 3. Is there an analogy that beats the jargon?

**Before**: "A closure retains a reference to its lexical scope even after the outer function has
returned."

**After**: "A closure is like a backpack. When a function is created inside another function, it
packs up the variables it needs and carries them around, even after the outer function is long
gone." Then, once that lands: "That's what people mean by a closure."

## 4. Is the why written where the reader will trip over it?

**Before**: A retry loop with no comment, three files away from a Slack thread that explains the
flaky API it's working around.

**After**: One line directly above the loop: `// this API drops ~2% of requests under load, retry
before failing`.

## 5. Is this reaching for clever when plain would do?

**Before**: `arr.reduce((a,c)=>({...a,[c.id]:c}),{})` to turn a list into a lookup table.

**After**: A plain `for` loop that builds the same object, or `Object.fromEntries(arr.map(item =>
[item.id, item]))` with a comment naming what it's for. Same result, no puzzle to solve first.

## 6. Could this be said in fewer words?

**Before**: "In order to accomplish the task of validating the user's input, we need to first
check whether or not the field is empty before proceeding to check its format."

**After**: "Check the field isn't empty, then check its format."

## 7. Does the comment earn its place?

**Before**: `// increment i by 1` above `i++`. Repeats the code, tells the reader nothing new.

**After**: No comment at all — the code already says it. Comments are reserved for the *why*, not
restating the *what*.
