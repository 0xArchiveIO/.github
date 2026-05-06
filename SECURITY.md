# Security

Report security issues privately through the repository security advisory flow or by contacting 0xArchive support.

Do not open public issues for:

- API keys, wallet secrets, or credentials
- Vulnerabilities that expose account, billing, export, or market-data access
- Prompt-injection or tool-scope issues in MCP, CLI, skill, or agent workflows
- Supply-chain problems in package install paths

Public agent tooling should start with the narrowest local scope that can make one authenticated request. Do not make a project-wide or team-wide MCP, CLI, or skill setup the default until the local path has returned a concrete 0xArchive result.
