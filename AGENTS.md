# AGENTS.md

## 项目
工业机器视觉作品集：缺陷检测、自动标注、部署基准。
Python 3.12，PyTorch，Ultralytics，OpenCV，pytest，ruff。

## 目录
- src/vision_portfolio/  源代码
- tests/                 测试，文件名和源码一一对应
- data/                  本地数据，不提交到 Git

## 命令
- 安装：pip install -e ".[dev]"
- 测试：pytest -q
- 检查：ruff check . && ruff format --check .

## 编码规则
- 每个公开函数都要有类型标注和文档字符串，写清输入格式和单位
- 框的坐标默认 (x1, y1, x2, y2)，单位像素；其他格式必须在函数名或参数里写明
- 图像默认 BGR、HWC、uint8；转换格式时必须写注释
- 用 logging，不用 print

## 禁止
- 不准吞掉异常（except: pass）
- 不准编造 API：不确定函数或参数是否存在，就直接说不确定
- 不准提交图片、模型权重、客户数据、公司内部资料
- 一次只改一个模块，单次改动不超过 200 行
- 不准为了让测试通过而去修改测试

## 完成标准
- pytest 和 ruff 全部通过
- 新功能必须附带测试，覆盖边界情况
- 回复里列出改了哪些文件、为什么改