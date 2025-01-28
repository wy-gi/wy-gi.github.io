# UV

### 安装

如果使用 brew

```sh
brew install uv
brew install rust
```

总是可以从官网安装(需要科学上网)
```sh
curl -LsSf https://astral.sh/uv/install.sh | sh
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

### tool

```sh
uv tool update-shell

uv tool install prefect --with 'httpx[socks]'
uv tool upgrade prefect
uv tool upgrade --all
```

### 生成 `requirements.txt`

```sh
uv pip freeze > requirements.txt
uv pip compile pyproject.toml -o requirements.txt
```
