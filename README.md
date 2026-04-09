# helmet-check
基于YOLO的安全帽佩戴检测系统~Python+2026原创+计算机毕设项目

## 项目简介
基于 YOLO 的智能安全帽佩戴检测平台，面向施工现场图片识别、检测记录管理与安全宣传信息展示等业务场景。系统后端采用 Flask 搭建 RESTful API 服务，结合数据库进行业务数据持久化存储，并通过 JWT 实现用户身份认证与接口访问控制。

在核心识别能力方面，系统集成了训练完成的 YOLOv8 安全帽检测模型 `best.pt`。用户上传现场图片后，后端首先完成文件格式与大小校验，将原始图片保存到本地媒体目录，然后调用 YOLO 模型执行目标检测，识别图片中的 `person`、`head`、`helmet` 等目标信息。检测完成后，系统会自动生成带标注框的结果图片，并提取检测框坐标、类别名称、置信度和统计结果，形成结构化检测数据返回前端展示。

![图片](https://oa-project-storage.oss-cn-hangzhou.aliyuncs.com/e681785ba8354ed999cc820c862d8447.png)
![图片](https://oa-project-storage.oss-cn-hangzhou.aliyuncs.com/ce641cda65234cac82af3ef1389e6074.png)
![图片](https://oa-project-storage.oss-cn-hangzhou.aliyuncs.com/31e7e4a781094db8987633758ca00dd1.png)

## 演示视频 and 完整代码 and 安装
地址：https://www.yuque.com/ziwu/qkqzd2/ah2aszdt5cegsfgv

