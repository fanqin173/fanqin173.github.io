---
title: "医院医疗管理效率分析：住院时长预测与优化"
collection: portfolio
type: "Data Analysis"
permalink: /portfolio/hospital-management-analysis
date: 2025-11-26
excerpt: "通过数据分析优化医院资源配置，提升运营效率"
header:
  teaser: /images/portfolio/hospital-management-analysis/department_distribution.png
tags:
  - 医院管理
  - 数据分析
  - 资源优化
tech_stack:
  - name: Python
  - name: Pandas
  - name: Matplotlib
  - name: Seaborn
---

# 医院医疗管理效率分析：住院时长预测与优化

## 项目背景
本项目旨在通过数据分析技术提升医院医疗管理效率，重点关注患者住院时长的预测与优化。通过对医院运营数据的深度挖掘，为资源配置和决策制定提供数据支持，最终实现运营效率的提升。

## 核心实现

### 数据预处理
```python
# 读取数据文件
df = pd.read_csv('Hospital_Data.csv')

# 处理缺失值与重复值
df.dropna(inplace=True)
df.reset_index(drop=True, inplace=True)
df.drop_duplicates(inplace=True)
df.reset_index(drop=True, inplace=True)

# 数据格式修正
df[['Age', 'Stay']] = df[['Age', 'Stay']].replace('Nov-20', '11-20')
