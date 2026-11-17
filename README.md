<!-- markdownlint-disable MD033 MD041 -->
<p align="center">
  <img alt="LOGO" src="https://cdn.jsdelivr.net/gh/MaaAssistantArknights/design@main/v1/icons/maa-logo_512x512.png" width="160" height="160" />
</p>

<div align="center">

# MaaVG

胜利女神：新的希望（NIKKE 国服）日常自动化脚本

</div>

基于 [MaaFramework](https://github.com/MaaXYZ/MaaFramework) 构建，通过图像识别 + Pipeline 驱动，完成每日固定流程。

## 脚本清单

| # | 脚本 | 文件 | 说明 |
|---|---|---|---|
| 1 | 启动游戏 | `nikke_launch.json` | 冷启动妮姬 → 关维护公告 → 点开始 → 停在大厅 |
| 2 | 跳过弹窗返回大厅 | `nikke_skip_popup.json` | 关闭进大厅后的活动公告弹窗，确认回到大厅 |
| 3 | 付费商店免费礼包 | `nikke_payshop.json` | 每日 / 每周免费礼包领取后回大厅 |
| 4 | 百货商店免费商品 | `nikke_shop.json` | 100% SALE 商品购买 → 刷新 → 再买 → 回大厅 |
| 5 | 前哨基地扫荡领奖 | `nikke_outpost.json` | 一举歼灭 / 领取保管箱奖励，红点驱动，领完关面板 |
| 6 | 派遣公告栏领奖派遣 | `nikke_dispatch.json` | 全部领取已完成派遣 → 全部派遣 → 回大厅 |
| 7 | 咨询批量咨询 | `nikke_consult.json` | 前哨基地 → 指挥中心 → 咨询 → 批量咨询 → 回大厅 |
| 8 | 好友赠送社交点数 | `nikke_friend.json` | 打开好友面板 → 赠送 → 关闭 |
| 9 | 任务领取每日奖励 | `nikke_task.json` | 每日任务「全部领取」两次（任务奖励 + POINT 宝箱） |
| 10 | 模拟室快速模拟 | `nikke_simulation.json` | 方舟 → 模拟室 → 开始模拟 → 快速模拟 → 结算 |
| 11 | 拦截战每周战斗 | `nikke_interception.json` | 次数判定 → 每周快速战斗 / 进入战斗 → 结算推进 |
| 12 | 无限之塔爬塔 | `nikke_tower.json` | 无限之塔 → 当前层 → 进入战斗 → 成败分支 → 回大厅 |
| 13 | 竞技场领奖与新人战 | `nikke_arena.json` | 特殊竞技场领累积奖励 + 新人竞技场免费战斗循环 |

## 使用方式

1. 安装 [MaaFramework](https://github.com/MaaXYZ/MaaFramework) 推荐的前端（如 MFAAvalonia）；
2. 加载本项目目录（`interface.json` 所在目录）；
3. 控制器选「安卓端」，资源选「国服（腾讯）」；
4. 任务列表按 1 → 13 顺序执行即可。

分辨率基准为 **720×1565**（`display_short_side: 720`），所有识别区与点击点均基于该坐标系。

## 目录结构

```
assets/
  interface.json          # Project Interface V2 任务/控制器/资源定义
  resource/
    pipeline/             # 13 个 nikke_*.json 流水线
```

## 许可

[MIT](LICENSE)
