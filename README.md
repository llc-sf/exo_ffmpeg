# ExoPlayer

**This GitHub project is deprecated.**  The latest version of ExoPlayer is
published as part of [AndroidX Media3][].

All users should migrate to AndroidX Media3. Please refer to our [migration
guide and script][] to move your codebase to the Media3 package names.

*   As of 2024-04-03 we have stopped pushing commits to the `dev-v2` branch in
    this repository. New ExoPlayer code is available in the AndroidX Media
    GitHub repository: https://github.com/androidx/media
*   `exoplayer:2.19.1` was the last artifact released from this project, we
    don't plan to release any more.

[AndroidX Media3]: https://github.com/androidx/media
[migration guide and script]: https://developer.android.com/guide/topics/media/media3/getting-started/migration-guide


NDK_PATH="/Users/chenlu/Library/Android/sdk/ndk/21.1.6352462"

FFMPEG_PATH="/Users/chenlu/work/exo/ExoPlayer-release-v2/extensions/ffmpeg/src/main/jni/ffmpeg"

ANDROID_ABI=21

ENABLED_DECODERS=(vorbis opus flac alac mp3 aac ac3 eac3 ape)

cd "${FFMPEG_MODULE_PATH}/jni" && \
./build_ffmpeg.sh \
"${FFMPEG_MODULE_PATH}" "${NDK_PATH}" "${HOST_PLATFORM}" "${ENABLED_DECODERS[@]}"
