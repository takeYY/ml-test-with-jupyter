# ml-test-with-jupyter

Jupyter Notebook を使った機械学習プログラム群

## コマンド関連

- 初回起動

```bash
docker run -v `pwd`:/home/jovyan/work -p 10000:8888 --name ml-jupyter jupyter/scipy-notebook
```

- 2 回目以降の起動

  - コンテナ起動

  ```bash
  docker start ml-jupyter
  ```

  - 状態を確認、STATUS: UP なら起動成功

  ```bash
  docker ps
  ```

  - トークンを確認された場合、コンテナに入ってログを出力

  ```bash
  docker exec -it ml-jupyter bash
  jupyter notebook list

      Currently running servers:
      http://localhost:8888/?token=<トークン>
  ```
