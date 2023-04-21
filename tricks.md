# tricks
## 批量下载所有网页中的图片
```
<!-- 控制台输入 -->
// 获取所有图片标签
const images = Array.from(document.querySelectorAll('img'));

// 定义一个函数，用于将图片链接转换成 Blob 对象
async function getImageBlob(url) {
  const response = await fetch(url);
  const blob = await response.blob();
  return blob;
}

// 定义一个函数，用于下载图片
async function downloadImage(url) {
  const blob = await getImageBlob(url);
  const imageUrl = URL.createObjectURL(blob);

  const link = document.createElement('a');
  link.href = imageUrl;
  link.download = url.split('/').pop();
  document.body.appendChild(link);
  link.click();
  document.body.removeChild(link);

  URL.revokeObjectURL(imageUrl);
}

// 遍历所有图片标签，调用 downloadImage 函数下载图片
images.forEach((img) => {
  downloadImage(img.src);
});

```
下载下来的图片格式混乱，写个.bat批量修改文件后缀
```
@echo off
setlocal EnableDelayedExpansion

for %%f in (*.*) do (
    set "filename=%%~nf"
    set "extension=.jpg"
    ren "%%f" "!filename!!extension!"
)

echo All files renamed.
pause
```

