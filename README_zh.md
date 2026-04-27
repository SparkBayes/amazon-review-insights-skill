# Amazon Review Insights

亚马逊评论智能分析工具，专为 Claude Code 代理设计。

## 功能特性

- **评论采集** - 支持 8 个亚马逊市场站点（US、CA、UK、DE、FR、IT、ES、JP）
- **AI 智能分析** - 自动识别和分类差评
- **问题量化** - 发现高频问题
- **隐藏反馈挖掘** - 从 5 星评论中发现隐藏的负面情绪
- **趋势追踪** - 监控评论趋势变化
- **增量更新** - 获取最新评论，避免重复数据

## 安装

```bash
pip install -r requirements.txt
```

## 配置

通过环境变量设置 API Key：

```bash
export CUSTOMER_INSIGHTS_API_KEY="your-api-key"
```

> 在 [astrmap.com](https://www.astrmap.com/) 获取 API Key - 用户菜单 → API Keys

## 使用方法

```bash
# 检查设备状态
python scripts/api_client.py --action check_device

# 创建分析任务
python scripts/api_client.py --action create_task --asin "B09V3KXJPB" --site US

# 查询结果
python scripts/api_client.py --action get_ai_insights --task-id "TSK_xxx"
```

详细文档请参阅 [SKILL.md](amazon-review-insights/SKILL.md)。

## 支持的市场站点

| 站点 | 语言 |
|------|------|
| US | 英语 |
| CA | 英语 |
| UK | 英语 |
| DE | 德语 |
| FR | 法语 |
| IT | 意大利语 |
| ES | 西班牙语 |
| JP | 日语 |

## License

MIT