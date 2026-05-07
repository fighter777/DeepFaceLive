# Startup Guide

This file documents a simple startup flow for this fork.

## Paths

- Repository: `<repo_root>`
- Windows venv: `<windows_venv>`

## 1. Start DeepFaceLive

Run the application from the project root with:

```powershell
<windows_venv>\Scripts\python.exe <repo_root>\main.py run DeepFaceLive --userdata-dir <userdata_dir>
```

If you want to disable CUDA:

```powershell
<windows_venv>\Scripts\python.exe <repo_root>\main.py run DeepFaceLive --userdata-dir <userdata_dir> --no-cuda
```

## 2. What `<userdata_dir>` means

This is the folder used by DeepFaceLive to store:

- settings
- downloaded models
- work files
- user presets

Example:

```text
D:\DeepFaceLive_userdata
```

## 3. Typical first use

Once the application is open:

1. Choose a source:
   - webcam
   - video file
2. Set the face detector.
3. Set the face marker.
4. Set the face swapper model.
5. Open `StreamOutput`.
6. Click the window button to show the live output window.

The visible output window is usually:

```text
DeepFaceLive output
```

## 4. Recording the result

DeepFaceLive is mainly a real-time application.

For a video demo, the simplest method is:

1. open the `DeepFaceLive output` window
2. capture that window with OBS
3. record the session in OBS

## 5. Placeholder reference

The values written between `<` and `>` are placeholders.
Replace them with your own values.

### `<repo_root>`

The Windows folder where the project is stored.

Example:

```text
D:\projects\DeepFaceLive
```

### `<windows_venv>`

The Windows virtual environment used to run DeepFaceLive.

It is the folder that contains:

- `Scripts\python.exe`
- installed Python packages

Example:

```text
D:\venvs\DeepFaceLive-py312
```

### `<userdata_dir>`

The user data folder used by the application at runtime.

Example:

```text
D:\DeepFaceLive_userdata
```

## 6. Environment file

The exact environment snapshot used for this setup is stored in:

```text
requirements.deepfacelive-py312.freeze.txt
```

## 7. Notes

- This project is a real-time application first, not a video rendering pipeline.
- For demonstrations, OBS capture is a normal workflow.
- If the application starts but no result is visible, check the `StreamOutput` module and open its output window.
