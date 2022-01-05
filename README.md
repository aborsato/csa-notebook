# csa-notebook
Sample of running notebooks

## Running Locally
The code below will start a jupyter notebook server listening to port `$PORT` and requires no password to connect.
> Note: please consider removing the `--NotebookApp.token=''` paramater. This setup is **not** intended for production use as it can be exploited to run arbitrary code in the server.
```bash
JUPYTER_PORT=8888
jupyter notebook --NotebookApp.allow_origin="https://${CODESPACE_NAME}-${JUPYTER_PORT}.githubpreview.dev" --port=${JUPYTER_PORT} --NotebookApp.port_retries=0 --NotebookApp.token=''
```
