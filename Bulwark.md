### Error

```javascript
TypeError: Cannot read property 'date' of null
    at Object.getBlockRewardDetails (/root/Helio-explorer/cron/carver2d.js:467:59)
    at processTicksAndRejections (internal/process/task_queues.js:97:5)
    at async syncBlocks (/root/Helio-explorer/cron/block.js:220:41)
    at async update (/root/Helio-explorer/cron/block.js:495:5)
Mon, 01 May 2023 04:48:04 GMT    ** Cron Exception*!
```

### Solution:

#### Edit file:

```javascript
/root/Helio-explorer/cron/carver2d.js
```
- add new line at : 462

```javascript
if (!stakeInputTxCarverMovement) continue;
```
