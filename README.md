# aliyun-oss-paste-image

VSCode扩展插件，在 Markdown 类型文件编辑过程中，支持一键上传截图到阿里云OSS并将图片粘贴到博文中。

详见博文：[aliyun-oss-paste-image 插件安装使用指南](https://www.lixl.cn/2020/021737756.html)。

## 理想的 Markdown 博文写作及发布体验

1. 截图后一键粘贴（ `Shift + p` ）并实时预览，内容编辑所见即所得。
2. `hexo g -d` 一键发布到多个托管平台（ 如Github + COS ）。
3. 自建的博客平台拥有超快的访问速度且几乎零成本。
4. 直接粘贴/导入 Markdown 博文到第三方平台（如知乎、简书、CSDN）。

推荐使用 [Typora](https://www.typora.io/) + [hexo-deployer-cos-cdn](https://www.lixl.cn/2020/020936412.html)插件 实现如上体验。

喜欢使用 VSCode 的话，可以通过本插件来提高博文撰写体验。

## 安装
在插件应用商店搜索 `aliyun-oss-paste-image` ，点击 `install` 安装。如图:

![插件检索及安装](https://pic.lixl.cn/2020/15da665cf0d5309abc2b054508b61d76.png)

## 使用

先截图/复制图片内容，然后在 markdown 文件编辑过程中，使用 `Shift + p` 一键上传并粘贴图片。

## 参数设置

- `region`: 地域。在阿里云对象存储的bucket概览中有EndPoint（地域节点），如 `oss-cn-beijing.aliyuncs.com` 中的 `oss-cn-beijing` 就是地域。
- `accessKeyId`: accessKeyId（RAM中生成的accessKeyId）
- `accessKeySecret`: accessKeySecret（RAM中生成的accessKeySecret）
- `bucket`: 输入bucket名称
- `remotePath`: 图片存储目录。例如希望的图片地址为 `http://${你的域名}/static/${filename}.png`，则填写 `static` ）
- `domain`: 阿里云oss域名，建议绑定自定义域名并开启CDN加速
- `localTempPath`: 本地临时文件路径（默认: /tmp/.aliyun-oss-paste-image）

## License

MIT

## 参考

- [vscode-aliyun-upload-image](https://marketplace.visualstudio.com/items?itemName=vvkee.aliyun-oss-upload-image)
