
# Project Overview Tool

This tool concatenates the contents of all files in a project directory into a single text file while excluding specified files and directories. Usefull when interating with llms.

## Requirements

- Python 3.x
- `tqdm` package for progress bars

You can install `tqdm` using pip:

```sh
pip install tqdm
```

## Usage

The tool accepts the following arguments:

- `--project` or `-p`: **Required.** The name of the project root folder.
- `--exclude` or `-x`: **Optional.** Files or directories to exclude (space-separated list).
- `--output` or `-o`: **Optional.** The output file name. Default is `tview.txt`.
- `--viewignore` or `-v`: **Optional.** Path to the `.viewignore` file. Default is `./tools/.viewignore`.

### Example

```sh
python tools/tview.py --project PROJECT_NAME
```

### Example with Optional Arguments

```sh
python tools/tview.py --project PROJECT_NAME --output overview.txt --exclude extra_file.txt extra_dir
```

In this example:
- `--project PROJECT_NAME`: Specifies the name of the project root folder.
- `--output overview.txt`: Specifies the output file name as `overview.txt`.
- `--exclude extra_file.txt extra_dir`: Excludes `extra_file.txt` and `extra_dir` from the overview.

## License

This project is licensed under the MIT License.
