Used this handy snippet to find some tests where a Promise rejection was being swallowed. 
Apparently later versions of Node will make this failure a lot noisier, so this snippet won't be needed.

```javascript
  process.on('unhandledRejection', (err) => {
      console.log('err', err);
      throw err;
  });
```
    
