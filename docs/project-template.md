# 面试项目元信息模板

当创建新的面试项目时，使用以下结构：

## meta.yaml 模板

```yaml
---
name: [公司名]-[岗位名]
description: [公司名] [岗位名] 面试项目
created_at: YYYY-MM-DD
updated_at: YYYY-MM-DD

company: [公司名]
position: [岗位名]
jd_source: [JD来源：内部推荐/官网/Boss直聘等]

status: pending
# 状态选项：
#   pending - 投递中，等待面试通知
#   interview_scheduled - 面试已安排
#   interview_completed - 面试完成，待复盘
#   reviewed - 复盘完成
#   offer_received - 收到 offer
#   rejected - 未通过

interview_rounds:
  - round: 1
    type: [技术面/业务面/HR面/综合面]
    scheduled_at: null
    status: pending
    result: null

resume_file: resume-generated.md
jd_file: JD.md
```

## 使用说明

1. 当用户告知简历投递成功时，在 `output/` 下创建项目文件夹
2. 初始化 `meta.yaml` 并填写基本信息
3. 复制 JD 和生成的简历到项目目录
4. 后续面试演练和复盘记录自动存入对应子目录
