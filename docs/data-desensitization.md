# Data Desensitization

本仓库所有示例均为脱敏或重绘材料。

## 已替换的信息

- 客户名称替换为 `Anonymous Manufacturing Company`；
- 品牌、Logo、系统名称和人员姓名全部移除；
- 真实 URL、服务器地址和目录路径全部替换；
- 真实表名替换为 `mfg_olap.*`、`mfg_dw.*`、`mfg_report.*`；
- 真实字段名替换为制造业通用字段；
- SQL 只保留结构示意，不保留生产查询全文；
- 截图为脱敏重绘图，不是原始客户截图。

## 保留的信息

- 制造业报表治理问题结构；
- 报表、数据集、源表、字段、参数、MCP 的关系；
- 资产盘点与 AI 查询的交互方式；
- 影响分析的产物形态。

## 发布前检查建议

```bash
rg -n -f sensitive-terms.txt .
git log --format='%h %an <%ae>' --all
```

其中 `sensitive-terms.txt` 可按实际项目临时维护，放入客户名、域名、人员姓名、服务器地址、密钥关键词等检查项；检查完成后不要提交该文件。
