# 办公小工具

使用 Python 编写各种能够提高工作效率的小工具，代码可供学习和使用，不可用于非法用途！  
~~目前发布的 EXE 可执行文件支持在 Win 10 直接运行，已知在 Win 7 无法正常运行。~~

*****

## 报告编辑部小工具

<details>
    <summary>安装依赖</summary>

* pip install pyperclip
* pip install pysimplegui

</details>

<details>
    <summary>使用说明</summary>

### 营养成分表计算

* 数值修约规则为四舍六入五成双。
* NRV%均使用修约数值进行计算。
* NRV%计算结果数值在0.5%~1.0%之间时均修约为1%。
* 从 Word 文档复制五项营养成分数值（包括单位），点击按钮可自动导入并填充数值。
* 输入数值点击计算，自动再次计算能量数值，计算公式为：能量=蛋白质×17+脂肪×37+碳水化合物×17。

### 脱水率限值计算

* 数值修约规则为四舍六入五成双。
* 点击常见样品按钮可自动填充部分数值。
* 已知脱水率时，鲜品水分输入100，本品水分输入脱水率数值即可。
* 脱水率计算公式：（鲜品水分-本品水分）÷（1-本品水分）
* 限值折算公式：项目限值÷（1-脱水率）
* 点击计算后，再次点击复制备注按钮可智能复制相对应的备注内容至剪贴板。

### 固体饮料限值计算

* 数值修约规则为四舍六入五成双。
* 限值折算结果最多保留四位小数。
* 点击常见固体饮料按钮可自动填充部分数值。
* 固体饮料限值折算公式：（（样品量+水）÷样品量）×项目限值
* 点击计算后，再次点击复制备注可智能复制相对应的备注内容至剪贴板。

### 常用内容剪贴板

* 点击按钮即可复制相对应的无格式文本至剪贴板。

</details>

## 印章检测小工具

<details>
    <summary>安装依赖</summary>

* pip install fitz
* pip install PyMuPDF
* pip install opencv-python
* pip install pysimplegui

</details>

<details>
    <summary>使用说明</summary>

**检测扫描件（PDF 格式）中每页是否存在红色圆形印章。**

程序检测完成后会在 PDF 文件所在文件夹生成同名 xlsx 文件，该文件包含检测结果。

程序默认仅保存异常结果，当生成的 xlsx 文件名称包含“_正常”后缀时说明该 PDF 文件均为正常页；当选择保存全部结果时，文件检测结果不会在 xlsx 文件名体现，需要打开 xlsx 文件查看完整检测结果。

|状态|含义|
|----|----|
|True|正常页，检测到印章|
|False|异常页，未检测到印章|
|None|未知页，红色内容过多，跳过检测|

</details>

<details>
    <summary>实现原理</summary>

待更新

</details>
