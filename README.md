# 购物助手

技能包位于 [`shopping-helper/`](shopping-helper/)。

核验在售商品、价格、卖家和交易条件默认使用当前 Agent 自带的浏览器：登录一次后在同一会话中完成全部商品页取证，才能拿到登录价、券后实付和库存。运行环境无自带浏览器时，可选安装 `web-access` skill 作为兜底；它不是必需依赖。

行为评估用例位于 [`shopping-helper/evals/cases.yaml`](shopping-helper/evals/cases.yaml)，覆盖隐式触发、购买必要性、购买时机、证据门槛、候选覆盖与停止条件，以及失败恢复。

在本项目中使用该 Skill 时，Agent 会按 [`AGENTS.md`](AGENTS.md) 自动把每次咨询和推荐结果记录到 `records/`。该目录只保存在本地，不提交到仓库。Claude Code 通过 `CLAUDE.md` 引用同一份规则。
