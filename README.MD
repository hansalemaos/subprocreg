# Execute apps using subprocess ([in]visible) + regedit.exe path search 

## pip install subprocreg

### Tutorial (Brazilian Portuguese)

[![YT](https://i.ytimg.com/vi/Tr_rFIrM4vM/maxresdefault.jpg)](https://www.youtube.com/watch?v=Tr_rFIrM4vM)
[https://www.youtube.com/watch?v=Tr_rFIrM4vM]()

#### Tested against Windows 10 / Python 3.10 / Anaconda


```python
    Args:
        file (str): The file to be opened by the application.
        path (str): The path to the application executable (file path/or reg path)
        exit_keys (str, optional): The key combination to exit the application. Defaults to "ctrl+alt+o".
        add_options (tuple, optional): Additional options to pass to the application. Defaults to ().
        headless (bool, optional): Whether to run the application in headless mode. Defaults to True.
        **kwargs: Additional keyword arguments to pass to the subprocess.Popen() function.

    Returns:
        subprocess.Popen: A Popen object representing the executed application process.
    Examples:
        from subprocreg import execute_app
        proc=execute_app(
            file=r"F:\4 Promille - Oi the Meeting.mp3",
            path=(r"HKEY_CLASSES_ROOT\Directory\shell\AddToPlaylistVLC", "Icon"),
            exit_keys="ctrl+q",
            add_options=(
                "--input-repeat=0",
                "-Idummy",
                "--play-and-exit",
                "--qt-minimal-view",
            ),
            headless=True,

        )
        proc=execute_app(
            file=r"C:\ProgramData\anaconda3\envs\dfdir\gracefully_kill.py",
            path=r"C:\Windows\System32\notepad.exe",
            exit_keys="ctrl+b",
            add_options=(),
            headless=False,

        )
```		
