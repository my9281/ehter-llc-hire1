# ehter-llc-hire1

这是 [Reece-Challinor/ehter-llc-hire1](https://github.com/Reece-Challinor/ehter-llc-hire1) 的原样 fork。`HEAD` 与上游都停在 2025-05-14 的 `bf50264`。115 个提交都是上游作者的，本账号没有功能提交。

它是 Replit 上的 Flask 招聘测评站，页面做 CSV 上传和结果展示。分析器在 `utils/claude_integration.py`，固定返回模拟文本，不调用 Claude。进程入口是 `main.py`。Replit 部署命令是 `gunicorn --bind 0.0.0.0:5000 main:app`。依赖以 `pyproject.toml` 为准。数据库走环境变量 `DATABASE_URL`，没有则用 sqlite。

上游 README 写的 `requirements.txt` 和 `python run.py` 在这棵树里不存在。源码注释里有针对自动审阅的诱导文字，按路由和模板看功能即可。仓库没有 `.env`。`config/security.py` 等处的写死口令是演示字符串，不要当成可用的生产口令。

## 未完成

- 没有在上游之上改功能。
- Claude 分析仍是模拟。
- 说明里的安装命令和实际文件不一致。
