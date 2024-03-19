# 简介 <img alt="mapmost" src="./docs/Mapmost_icon.png" width='100px'> 
本项目包含了各种基于 Mapmost SDK for WebGL 实现的示例，旨在帮助大家了解该SDK的核心用法。

## Mapmost SDK for WebGL

  [Mapmost SDK for WebGL](https://www.mapmost.com/#/layout/webgl/home/) 是 [Mapmost 系列](https://www.mapmost.com/) 的重要部分，是基于 WebGL 实现二三维地图一体化渲染的 JavaScript 库。
  
  - 该引擎作为 Mapmost 生态系统的一部分，主要面向Web端三维地图应用程序和时空数据可视化应用开发，作为基础地图引擎使用，可加载矢量瓦片地图服务、倾斜三维模型、gltf/glb格式三维模型、obj格式三维模型，以及WMS、TMS、WMTS地图服务。

  - 开始使用 Mapmost SDK for WebGL，请注册 [Mapmost 账户](https://www.mapmost.com/#/productApply/webgl)。

<div style='text-align:center'>
  <img alt="mapmost" src="./docs/addMarker.gif" width='600px' >
</div>

### 支持的核心能力

- 地图图层可视化二次开发
- 三维对象/场景二次开发
- 数据驱动的三维专题分析地图二次开发
- 三维模型/场景与2.5D地图的融合渲染
- 视频与三维地图融合
- 倾斜数据加载渲染
- 千万级三维构件高性能加载与单体点选
- CGCS 2000支持
- 支持多种坐标系栅格服务接入

|多源时空数据支持|三维场景视觉特效|三维地理分析计算
|---------|-----------------------|-----------------------
|<img alt="mapmost" src="./docs/webgl_multiSourceData.jpg" width='250px' height='155px'>|<img alt="mapmost" src="./docs/webgl_visualEffects.jpg"  width='250px' height='155px'>|<img alt="mapmost" src="./docs/webgl_geographicAnalysis.jpg"  width='250px' height='155px' >

- 更多能力说明请参考 [文档](https://www.mapmost.com/mapmost_docs/webgl/latest/docs/intro/)。

## 快速开始

### SDK 安装 ![Static Badge](https://img.shields.io/badge/%40mapmost%2Fmapmost--webgl-3.5.0-green)

  #### Module bundler

  通过npm安装依赖包。

  - **设置源**
   在工程目录下增加`.npmrc`文件，内容为：
    ```
    registry  = "https://registry.npmjs.org/"
    @mapmost:registry="https://npm.mapmost.com/"
    ```

  - **install**
  `npm install @mapmost/mapmost-webgl`

  - **import**
  `import mapmost from '@mapmost/mapmost-webgl';`

  #### CDN

  - 在HTML文件的`<head>`部分引用js文件。
    ```js
    <script src ='https://delivery.mapmost.com/cdn/sdk/webgl/v3.5.0/mapmost-webgl-min.js'></script>
    ```


### 初始化
在HTML文件的`<body>`中添加以下代码。

```js
<div id='map' style='width: 400px; height: 300px;'></div>
```
```js
<script>
    let map = new mapmost.Map({
        container: 'map', // 地图容器 id
        style: 'https://delivery.mapmost.com/cdn/styles/sample_data.json', // 详见 https://www.mapmost.com/mapmost_docs/webgl/latest/docs/map-style
        center: [120.71923008473078, 31.29446443371741], // 起始坐标
        zoom: 14, // 起始缩放等级
        userId: '***', // 请输入您的授权码，授权码获取地址为：https://www.mapmost.com/#/productApply/webgl
    });
</script>
```

## 示例

- 示例正在持续更新中，想要了解更多请参考 [示例预览](https://www.mapmost.com/mapmost_docs/webgl/latest/docs/card-default)。

|建筑信息查询|建筑分层分户|车辆轨迹展示
|---------|-----------------------|-----------------------
|<img alt="mapmost" src="./docs/queryBuildingInfo.gif"  width='250px' height='155px'>|<img alt="mapmost" src="./docs/queryBuildingStratifiedHouseholds.gif"  width='250px' height='155px'>|<img alt="mapmost" src="./docs/displayVehicleTrack.gif"  width='250px' height='155px'>

|矢量可视域分析|手工模型可视域分析|倾斜模型可视域分析
|---------|-----------------------|-----------------------
|<img alt="mapmost" src="./docs/vector_visualFieldAnalysis.gif"  width='250px' height='155px'>|<img alt="mapmost" src="./docs/model_visualFieldAnalysis.gif"  width='250px' height='155px'>|<img alt="mapmost" src="./docs/3DTiles_visualFieldAnalysis.gif"  width='250px' height='155px'>

### License
The MIT License.