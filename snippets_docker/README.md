# jupyter/docker-stacks snippets

#### Select a jupyter/docker-stacks from this [list of available images](https://github.com/jupyter/docker-stacks/blob/master/docs/using/selecting.md).

#### How to download and install a image

```
docker pull [OWNER/IMAGE_NAME:TAG]

# Example:
docker pull jupyter/minimal-notebook:latest
```

#### How to run Jupyter Lab

```
cd [FOLDER_NAME]
docker run --rm -p 8888:8888 -e JUPYTER_ENABLE_LAB=yes -v ${PWD}:/current_directory -w /current_directory [IMAGE_NAME_OR_ID:TAG]
```

#### How to run a Python script

```
cd [FOLDER_NAME]
docker run --rm -v ${PWD}:/current_dir -w /current_dir [IMAGE_NAME_OR_ID:TAG] python [SCRIPT_NAME].py
```

#### How to run multiple Python scripts

```
cd [FOLDER_NAME]
docker run -it --rm -v ${PWD}:/current_dir -w /current_dir [IMAGE_NAME_OR_ID:TAG] /bin/bash
python [SCRIPT_NAME_1].py
python [SCRIPT_NAME_2].py
(...)
```
