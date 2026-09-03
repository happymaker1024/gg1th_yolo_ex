# yolo_roboflow
roboflow기반 yolo활용

# 가상환경 만들기
```
uv init --bare --name yolo-ex
```

# 주피터 노트북 환경만들기
```
uv add ipykernel
uv run python -m ipykernel install --user --name .venv
```

# uv 가상환경에 torch cuda 버전 설치하기
- pyproject.toml 환경셋팅
```
[[tool.uv.index]]
name = "pytorch-cu126"
url = "https://download.pytorch.org/whl/cu126"
explicit = true

[tool.uv.sources]
torch = { index = "pytorch-cu126" }
torchvision = { index = "pytorch-cu126" }
```

- torch 설치하기
```
uv add torch torchvision
```

# 라이브러리 설치
```
uv add inference-sdk
uv add python-dotenv
uv add roboflow
uv add "opencv-python==4.12.0.88"
```
