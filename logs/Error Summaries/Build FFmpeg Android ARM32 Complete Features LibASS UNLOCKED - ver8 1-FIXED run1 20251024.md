# FFmpeg Build Error Summary

## Workflow Info

- **Name:** Build FFmpeg Android ARM32 (Complete Features + LibASS UNLOCKED - ver8.1-FIXED)
- **Run:** #1
- **Version:** ver8
- **Date:** 2025-10-24 04:09:31
- **Status:** Failed
- **GitHub:** https://github.com/share-18001080/113/actions/runs/18769214535

## AI Analysis (Gemini 2.0 Flash)

```json
{
"error_id": "ERROR-001",
"error_name": "CMake Deprecation Warning: CMake < 3.10 compatibility removed.",
"root_cause": "The CMake version used is older than 3.10, and the android-legacy.toolchain.cmake file is deprecated.",
"affected_library": "libass",
"error_type": "CONFIGURE",
"symptoms": ["CMake Deprecation Warning during configuration."],
"fix_suggestion": "Update the CMake version to 3.10 or higher. Alternatively, update the CMakeLists.txt file to be compatible with newer CMake versions and remove the dependency on the deprecated android-legacy.toolchain.cmake. Check the NDK documentation for the recommended CMake configuration.",
"confidence": 90
}
```

### Error Details

**Error ID:** ERROR-001
**Error Name:** CMake Deprecation Warning: CMake < 3.10 compatibility removed.
**Affected Library:** libass
**Error Type:** CONFIGURE
**AI Confidence:** 90%

**Symptoms:**

- CMake Deprecation Warning during configuration.

**Root Cause:**

The CMake version used is older than 3.10, and the android-legacy.toolchain.cmake file is deprecated.

**Fix Suggestion:**

Update the CMake version to 3.10 or higher. Alternatively, update the CMakeLists.txt file to be compatible with newer CMake versions and remove the dependency on the deprecated android-legacy.toolchain.cmake. Check the NDK documentation for the recommended CMake configuration.

## Error Context (20 lines before exit code)

```
2025-10-24T04:09:11.9237848Z   /home/runner/work/113/113/external/x265/build/linux/CMakeFiles/CMakeScratch/TryCompile-P0SxFp/CMakeLists.txt:5 (project)
2025-10-24T04:09:11.9238337Z 
2025-10-24T04:09:11.9238342Z 
2025-10-24T04:09:11.9240472Z CMake Deprecation Warning at /opt/hostedtoolcache/ndk/r25c/x64/build/cmake/android-legacy.toolchain.cmake:34 (cmake_minimum_required):
2025-10-24T04:09:11.9241135Z   Compatibility with CMake < 3.10 will be removed from a future version of
2025-10-24T04:09:11.9241452Z   CMake.
2025-10-24T04:09:11.9241542Z 
2025-10-24T04:09:11.9241724Z   Update the VERSION argument <min> value.  Or, use the <min>...<max> syntax
2025-10-24T04:09:11.9242149Z   to tell CMake that the project requires at least <min> but has been updated
2025-10-24T04:09:11.9242514Z   to work with policies introduced by <max> or earlier.
2025-10-24T04:09:11.9242788Z Call Stack (most recent call first):
2025-10-24T04:09:11.9243185Z   /opt/hostedtoolcache/ndk/r25c/x64/build/cmake/android.toolchain.cmake:54 (include)
2025-10-24T04:09:11.9243777Z   /home/runner/work/113/113/external/x265/build/linux/CMakeFiles/3.31.6/CMakeSystem.cmake:6 (include)
2025-10-24T04:09:11.9244737Z   /home/runner/work/113/113/external/x265/build/linux/CMakeFiles/CMakeScratch/TryCompile-P0SxFp/CMakeLists.txt:5 (project)
2025-10-24T04:09:11.9245207Z 
2025-10-24T04:09:11.9245211Z 
2025-10-24T04:09:11.9838140Z -- Looking for strtok_r - found
2025-10-24T04:09:11.9851833Z -- Configuring done (2.1s)
2025-10-24T04:09:12.0035258Z -- Generating done (0.0s)
2025-10-24T04:09:12.0039066Z -- Build files have been written to: /home/runner/work/113/113/external/x265/build/linux
2025-10-24T04:09:12.0091778Z ##[error]Process completed with exit code 1.
```


---

**For Perplexity:** Read this summary in the `logs/Error Summaries/` folder and suggest detailed fix steps.
