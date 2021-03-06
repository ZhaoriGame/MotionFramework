### 资源包收集工具 (AssetBundleCollector)

![image](https://github.com/gmhevinci/MotionFramework/raw/master/Docs/Image/AssetBundleCollector1.png)

**界面说明**  
不同项目对资源的处理及打包规则都有所不同，我们可以通过以下几项设置来定制化自己的打包规则。  
1. Collect : 收集文件夹内资源进行打包（包括所有子文件夹）
2. Ignore : 忽略文件夹内资源不参与打包（包括所有子文件夹）
3. TagByFilePath : AssetBundle标签按照文件路径设置
4. TagByFolderPath : AssetBundle标签按照文件所在的文件夹路径设置
5. TagByFileName : AssetBundle标签按照文件名字设置
6. TagByFolderName : AssetBundle标签按照文件所在的文件夹名字设置  

注意：TagByFolder会将文件夹内所有资源打在一个AssetBundle文件里。

**什么是变体**  
通过构建变体AssetBundle文件，我们可以使用不同变体的AssetBundle并自由切换它们。例如：高清特效纹理，普通特效纹理；中文艺术字，日文艺术字，韩文艺术字。  
在游戏运行时，可以通过MotionFramework提供的接口设置要使用的变体类型，开发者不用关心这些变体资源的引用关系。

**构建变体的步骤说明**  
1. 修改资源的文件夹名称，在末尾加入变体类型后缀
2. 设置该资源文件夹或父类文件夹的收集方式为：TagByFolderPath
![image](https://github.com/gmhevinci/MotionFramework/raw/master/Docs/Image/AssetBundleCollector2.png)
![image](https://github.com/gmhevinci/MotionFramework/raw/master/Docs/Image/AssetBundleCollector3.png)

**构建变体的注意事项**  
1. 资源的文件名和文件格式必须一致，否则会造成构建包内该资源的唯一ID不一致，资源关联会失败。