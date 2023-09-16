- ⚠️注意：以下代码均为伪代码。
  Vue+html2canvas：[参考](https://github.com/niklasvh/html2canvas)
  ```
  html2canvas(htmlString)
  	.then(canvas => canvas.toDataURL(imgPatth));
  ```
  Nodejs+node-webshot：[参考](https://github.com/brenden/node-webshot)
  ```
  webshot(ssr(htmlPath)->htmlString, imgPath);
  ```
  Nodejs+puppeteer：[参考](https://pptr.dev/api/puppeteer.page.screenshot)
  ```
  (new puppeteer.Page())
  	.content(ssr(html))
      	.screenshot();
  ```
  Electron：[参考](https://www.geeksforgeeks.org/printing-in-electronjs/)
  ```
  (new BrowserWindow())
  	.webContents.loadUrl(htmlPath)
          .print();
  ```
  Electron+puppeteer：[参考](https://www.npmjs.com/package/puppeteer-in-electron)
  ```
  (new puppeteerInElecton.Page())
  	.content(ssr(htmlPath)->htmlString)
      	.screenshot();
  ```