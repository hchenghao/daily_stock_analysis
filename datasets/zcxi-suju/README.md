# zcxi/suju A股日线数据镜像

本目录记录 Hugging Face 数据集 `zcxi/suju` 的镜像规则。

## 镜像文件

只镜像数据集卡指定的 canonical 文件：

- 文件：`merged_stock.parquet`
- SHA-256：`8d93f3e15d5ad5931776a5e313493103b82fe0ca74d50b116ed399530433e622`
- 行数：8,327,981
- 股票代码数量：8,827
- 日期范围：2021-08-02 至 2026-02-02
- 字段：`Date`, `Open`, `High`, `Low`, `Close`, `Amount`, `Vol`, `StockCode`

Hugging Face 仓库中还有多个历史或实验版本。Dataset Viewer 会把多个
Parquet 文件共同统计为约 34.4M 行。为避免重复和版本混用，本镜像不把
这些版本合并上传。

## 存储方式

主文件约188MB，超过GitHub普通Git文件100MiB限制，因此通过GitHub
Release资产保存，不写入Git历史。

Release tag：

`dataset-zcxi-suju-2026-02-02`

## 运行

将本包内容复制到仓库根目录并推送到 `main`。工作流文件首次推送后会自动
运行，也可以在Actions页面手动运行：

`Mirror zcxi suju dataset to Release`

## 来源和许可

- 原始数据集：https://huggingface.co/datasets/zcxi/suju
- 原作者 / 维护者：zcxi
- 许可：CC BY 4.0

使用或再分发时请保留原作者、原始数据集链接和许可说明。
