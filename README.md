# 广州某高校经典诵读脚本

- 根据 [Steve0x2a](https://github.com/Steve0x2a/GZHU_JDSD)
  的源码和 [LihaoLikeOrangeJuice](https://github.com/LihaoLikeOrangeJuice/clockIn_gzhu) 的 Actions 思路修改
- 仅用作学习交流，本项目不承担任何风险和后果

## 添加功能

1. 使用 GitHub Actions 完成
2. 添加 [pushplus](https://www.pushplus.plus/) 推送支持

## 使用方法

1. 不会设置 Actions secrets 请参考[此项目](https://github.com/LihaoLikeOrangeJuice/clockIn_gzhu)
2. 抓取该小程序的 key 参数，在 Actions secrets 添加 `KEY` 参数
3. 推送可以使用
    - pushplus，在 Actions secrets 添加 `TOKEN` 参数
    - [server酱](https://sct.ftqq.com)，在 Actions secrets 添加 `SKEY` 参数
    - bark，在 Actions secrets 添加 `BURL` 参数（未测试，没有iOS设备）
4. 每天定时运行，目前为上午7点，可以修改 [jdsd.yml](https://github.com/1DoubleHelix/jdsd-clockln/blob/main/.github/workflows/jdsd.yml)
   的 `cron` 参数决定运行时间
5. Actions 运行时间依据 GMT 时间，需要向后推8小时，东八区每天早上7点示例如下

```yaml
on:
  schedule:
    - cron: '0 23 * * *'
```

## 其他

1. 抓取 key 的方法请自行检索
2. Actions 运行时间可能会有延后
3. 或许会因为不可抗力删除项目，仅作交流学习，请勿过分依赖
4. 如有帮助希望点亮star

