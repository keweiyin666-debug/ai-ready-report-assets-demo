# Manufacturing BI Report Sample

这是一个脱敏制造业报表示例，用于说明报表资产解析后的结构。

## 报表名称

PO-SO 一致性分析报表

## 业务场景

用于对比销售订单与采购订单在客户、物料、数量、交付日期和销售组等维度上的一致性，辅助分析订单交付异常、采购执行偏差和供应链协同问题。

## 常见查询问题

- 某个客户的订单为什么交付延迟？
- PO 与 SO 的数量为什么不一致？
- 某个物料号在哪些报表中被使用？
- 如果修改订单明细视图，会影响哪些分析报表？
- 这个报表的数据口径是什么？

## 报表结构示意

```text
Report: PO-SO 一致性分析
  Datasets:
    - head_po
    - head_salesman
    - head_customer
    - po_so_detail
  Source tables/views:
    - mfg_olap.v_order_sales_detail
    - mfg_olap.v_purchase_order_detail
    - mfg_dw.dim_customer
    - mfg_dw.dim_material
  Output fields:
    - so_num
    - po_num
    - customer_name
    - material_code
    - delivery_date
    - consistency_result
```

