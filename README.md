# tshift

`tshift` is a versatile command-line tool for manipulating file timestamps and computing time differences between files.

## Features

- Shift file timestamps (creation and modification times) forward or backward
- Compute time differences between two files
- Support for macOS-specific timestamp manipulation
- Flexible time duration format

## Installation

1. Ensure you have Python 3.6 or later installed on your system.
2. Download the `tshift.py` script to your preferred location.
3. Make the script executable:
   ```
   chmod +x tshift.py
   ```
4. Optionally, create a symlink to run `tshift` from anywhere:
   ```
   ln -s /path/to/tshift.py /usr/local/bin/tshift
   ```

## Usage

### Shifting Timestamps

To shift timestamps forward:
```
tshift path/to/file.txt 3d5h
```
This shifts the file's timestamps forward by 3 days and 5 hours.

To shift timestamps backward:
```
tshift path/to/file.txt 3d5h --backward
```
This shifts the file's timestamps backward by 3 days and 5 hours.

### Computing Time Differences

To compute the time difference between two files:
```
tshift path/to/file1.txt path/to/file2.txt --diff
```
This displays the time difference between the two files in a human-readable format.

### Time Duration Format

The time duration can be specified using a combination of:
- `d` for days
- `h` for hours
- `m` for minutes
- `s` for seconds

Examples:
- `1d6h30m`: 1 day, 6 hours, and 30 minutes
- `2h45m`: 2 hours and 45 minutes
- `30s`: 30 seconds

## Notes

- On macOS, `tshift` uses the `SetFile` command to modify both creation and modification times. Ensure you have the necessary permissions and developer tools installed.
- On other systems, only the modification time can be changed.
- When computing time differences, the tool uses the creation time if available, otherwise it falls back to the modification time.

## Error Handling

`tshift` provides informative error messages for common issues such as:
- File not found
- Permission denied
- Invalid duration format

## Contributing

Contributions to `tshift` are welcome! Please feel free to submit pull requests or create issues for bugs and feature requests.

## License

This project is open source and available under the [MIT License](LICENSE).


## Note from Human

Code and this README entirely generated using AI.

[Prompts](https://www.perplexity.ai/search/write-a-python-cli-tool-to-shi-5NxHFpbERX.MTxLuzaXRqw)

