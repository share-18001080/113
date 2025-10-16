# 📚 FFmpeg Android ARM32 - Error Knowledge Base

> **Mục đích:** Tự động ghi lại toàn bộ lỗi build để tránh lặp lại sai lầm
> 
> **Cập nhật:** Tự động bởi GitHub Actions
> 
> **Tổng số lỗi:** 2

---

## 📋 Quick Reference

| ID | Tên lỗi | Tần suất | Workflow | Ngày |
| ERROR-902 | Build failed - See details | 1x | Build FFmpeg Android ARM32 (Full Features + LibASS Added - ver8) | 2025-10-16 |
| ERROR-900 | Build failed - See details | 1x | Build FFmpeg Android ARM32 (Full Features + LibASS Added - ver8) | 2025-10-16 |
|----|---------|----------|----------|------|

---

## 🔴 Chi tiết lỗi


### 🔴 ERROR-900: Build failed - See details

**📅 Ngày phát hiện:** 2025-10-16

**📦 Workflow:** Build FFmpeg Android ARM32 (Full Features + LibASS Added - ver8)

**🔢 Run:** [#3](https://github.com/share-18001080/113/actions/runs/18552116212)

**🎯 Tần suất:** Lần thứ 1 gặp lỗi này

**⚠️ Triệu chứng:**
```bash
2025-10-16T06:17:40.8480766Z [36;1m  echo "⚠️ Parallel build failed, trying single-threaded..."[0m
2025-10-16T06:17:40.8482147Z [36;1m    echo "⚠️ Build failed, trying with reduced optimizations..."[0m
2025-10-16T06:17:40.8483246Z [36;1m    make V=1 || echo "❌ LibAV1 build failed completely"[0m
2025-10-16T06:17:40.8484826Z [36;1m  echo "⚠️ Standard installation failed, trying manual installation..."[0m
2025-10-16T06:17:40.8494103Z [36;1m  echo "❌ LibAV1 build failed"[0m
2025-10-16T06:18:48.6181517Z [36;1m  echo "⚠️ Parallel build failed, trying single-threaded..."[0m
2025-10-16T06:18:48.6182114Z [36;1m  make V=1 2>&1 | tee build-single.log || echo "Single-threaded also failed"[0m
2025-10-16T06:19:48.0425822Z [36;1m  echo "⚠️ Parallel build failed, trying single-threaded..."[0m
2025-10-16T06:19:48.0427551Z [36;1m    echo "❌ LibSOXR build failed"[0m
2025-10-16T06:19:48.0438409Z [36;1m  echo "❌ LibSOXR build failed completely"[0m
2025-10-16T06:19:50.9039217Z [36;1m  echo "⚠️ Parallel build failed, trying single-threaded..."[0m
2025-10-16T06:19:50.9045916Z [36;1m  echo "❌ LibASS build failed - attempting manual copy"[0m
2025-10-16T06:19:51.4225303Z meson.build:1:0: ERROR: Unknown options: "harfbuzz, libtool"
2025-10-16T06:19:48.0425820Z [36;1m  echo "⚠️ Parallel build failed, trying single-threaded..."[0m
2025-10-16T06:19:48.0427549Z [36;1m    echo "❌ LibSOXR build failed"[0m
2025-10-16T06:19:48.0438407Z [36;1m  echo "❌ LibSOXR build failed completely"[0m
2025-10-16T06:19:50.9039215Z [36;1m  echo "⚠️ Parallel build failed, trying single-threaded..."[0m
2025-10-16T06:19:50.9045913Z [36;1m  echo "❌ LibASS build failed - attempting manual copy"[0m
2025-10-16T06:19:51.4224984Z meson.build:1:0: ERROR: Unknown options: "harfbuzz, libtool"
2025-10-16T06:17:40.8480763Z [36;1m  echo "⚠️ Parallel build failed, trying single-threaded..."[0m
```

**📋 Context (100 dòng cuối log):**
```
2025-10-16T06:19:26.5767573Z   CC       silk/fixed/noise_shape_analysis_FIX.lo
2025-10-16T06:19:26.5881058Z   CC       silk/fixed/process_gains_FIX.lo
2025-10-16T06:19:26.6280354Z   CC       silk/fixed/regularize_correlations_FIX.lo
2025-10-16T06:19:26.6639110Z   CC       silk/fixed/residual_energy16_FIX.lo
2025-10-16T06:19:26.7054951Z   CC       silk/fixed/residual_energy_FIX.lo
2025-10-16T06:19:26.7340394Z   CC       silk/fixed/warped_autocorrelation_FIX.lo
2025-10-16T06:19:26.7689123Z   CC       silk/fixed/apply_sine_window_FIX.lo
2025-10-16T06:19:26.7803347Z   CC       silk/fixed/autocorr_FIX.lo
2025-10-16T06:19:26.8162537Z   CC       silk/fixed/burg_modified_FIX.lo
2025-10-16T06:19:26.8505446Z   CC       silk/fixed/k2a_FIX.lo
2025-10-16T06:19:26.8727927Z   CC       silk/fixed/k2a_Q16_FIX.lo
2025-10-16T06:19:26.8748585Z   CC       silk/fixed/pitch_analysis_core_FIX.lo
2025-10-16T06:19:26.9494996Z   CC       silk/fixed/vector_ops_FIX.lo
2025-10-16T06:19:26.9756886Z   CC       silk/fixed/schur64_FIX.lo
2025-10-16T06:19:27.0070959Z   CC       silk/fixed/schur_FIX.lo
2025-10-16T06:19:27.0652649Z   CC       src/opus.lo
2025-10-16T06:19:27.0899661Z   CC       src/opus_decoder.lo
2025-10-16T06:19:27.1013883Z   CC       src/opus_encoder.lo
2025-10-16T06:19:27.1217513Z   CC       src/extensions.lo
2025-10-16T06:19:27.2107419Z src/extensions.c:504:18: warning: variable 'trailing_short_len' set but not used [-Wunused-but-set-variable]
2025-10-16T06:19:27.2108423Z       opus_int32 trailing_short_len;
2025-10-16T06:19:27.2108862Z                  ^
2025-10-16T06:19:27.2182422Z   CC       src/opus_multistream.lo
2025-10-16T06:19:27.3120241Z 1 warning generated.
2025-10-16T06:19:27.3235341Z   CC       src/opus_multistream_encoder.lo
2025-10-16T06:19:27.3325852Z   CC       src/opus_multistream_decoder.lo
2025-10-16T06:19:27.3391909Z   CC       src/repacketizer.lo
2025-10-16T06:19:27.5045147Z   CC       src/opus_projection_encoder.lo
2025-10-16T06:19:27.5141229Z   CC       src/opus_projection_decoder.lo
2025-10-16T06:19:27.5757681Z   CC       src/mapping_matrix.lo
2025-10-16T06:19:27.5982943Z   CC       src/analysis.lo
2025-10-16T06:19:27.6400009Z   CC       src/mlp.lo
2025-10-16T06:19:27.6473286Z   CC       src/mlp_data.lo
2025-10-16T06:19:27.7235802Z   CPPAS    celt/arm/celt_pitch_xcorr_arm-gnu.lo
2025-10-16T06:19:27.7940867Z   CCLD     libarmasm.la
2025-10-16T06:19:27.8906827Z   CCLD     libopus.la
2025-10-16T06:19:28.5988216Z make[2]: Leaving directory '/home/runner/work/113/113/external/opus'
2025-10-16T06:19:28.5993470Z make[1]: Leaving directory '/home/runner/work/113/113/external/opus'
2025-10-16T06:19:28.6401183Z make  install-recursive
2025-10-16T06:19:28.6691355Z make[1]: Entering directory '/home/runner/work/113/113/external/opus'
2025-10-16T06:19:28.7120505Z make[2]: Entering directory '/home/runner/work/113/113/external/opus'
2025-10-16T06:19:28.7382522Z make[3]: Entering directory '/home/runner/work/113/113/external/opus/doc'
2025-10-16T06:19:28.7383163Z make[3]: Nothing to be done for 'all'.
2025-10-16T06:19:28.7383747Z make[3]: Leaving directory '/home/runner/work/113/113/external/opus/doc'
2025-10-16T06:19:28.7681629Z make[3]: Entering directory '/home/runner/work/113/113/external/opus'
2025-10-16T06:19:28.7944208Z  /usr/bin/mkdir -p '/home/runner/work/113/113/external/../build/external/share/aclocal'
2025-10-16T06:19:28.7972725Z  /usr/bin/mkdir -p '/home/runner/work/113/113/external/../build/external/lib/pkgconfig'
2025-10-16T06:19:28.7973707Z  /usr/bin/mkdir -p '/home/runner/work/113/113/external/../build/external/include/opus'
2025-10-16T06:19:28.7974522Z make[4]: Entering directory '/home/runner/work/113/113/external/opus/doc'
2025-10-16T06:19:28.7977924Z  /usr/bin/install -c -m 644 opus.pc '/home/runner/work/113/113/external/../build/external/lib/pkgconfig'
```

**🔍 Nguyên nhân gốc rễ:**
- [ ] TODO: Cần phân tích thủ công
- Loại lỗi: Unknown

**🛠️ Fix đã thử:**
- [ ] TODO: Cập nhật sau khi thử fix

**📝 Status:** 🔴 Chưa fix

**🏷️ Tags:** `Unknown` `auto-generated` `run-3`

---


### 🔴 ERROR-902: Build failed - See details

**📅 Ngày phát hiện:** 2025-10-16

**📦 Workflow:** Build FFmpeg Android ARM32 (Full Features + LibASS Added - ver8)

**🔢 Run:** [#4](https://github.com/share-18001080/113/actions/runs/18554378999)

**🎯 Tần suất:** Lần thứ 1 gặp lỗi này

**⚠️ Triệu chứng:**
```bash
2025-10-16T08:01:41.1345651Z [36;1m  echo "⚠️ Parallel build failed, trying single-threaded..."[0m
2025-10-16T08:01:41.1346985Z [36;1m    echo "⚠️ Build failed, trying with reduced optimizations..."[0m
2025-10-16T08:01:41.1348057Z [36;1m    make V=1 || echo "❌ LibAV1 build failed completely"[0m
2025-10-16T08:01:41.1349595Z [36;1m  echo "⚠️ Standard installation failed, trying manual installation..."[0m
2025-10-16T08:01:41.1358633Z [36;1m  echo "❌ LibAV1 build failed"[0m
2025-10-16T08:02:50.4822110Z [36;1m  echo "⚠️ Parallel build failed, trying single-threaded..."[0m
2025-10-16T08:02:50.4822679Z [36;1m  make V=1 2>&1 | tee build-single.log || echo "Single-threaded also failed"[0m
2025-10-16T08:03:51.6472372Z [36;1m  echo "⚠️ Parallel build failed, trying single-threaded..."[0m
2025-10-16T08:03:51.6473867Z [36;1m    echo "❌ LibSOXR build failed"[0m
2025-10-16T08:03:51.6484821Z [36;1m  echo "❌ LibSOXR build failed completely"[0m
2025-10-16T08:03:54.7768364Z [36;1m  echo "⚠️ Parallel build failed, trying single-threaded..."[0m
2025-10-16T08:03:54.7775296Z [36;1m  echo "❌ LibASS build failed - attempting manual copy"[0m
2025-10-16T08:03:55.6331601Z meson.build:1:0: ERROR: Unknown options: "harfbuzz, libtool"
2025-10-16T08:03:51.6472369Z [36;1m  echo "⚠️ Parallel build failed, trying single-threaded..."[0m
2025-10-16T08:03:51.6473864Z [36;1m    echo "❌ LibSOXR build failed"[0m
2025-10-16T08:03:51.6484817Z [36;1m  echo "❌ LibSOXR build failed completely"[0m
2025-10-16T08:03:54.7768361Z [36;1m  echo "⚠️ Parallel build failed, trying single-threaded..."[0m
2025-10-16T08:03:54.7775293Z [36;1m  echo "❌ LibASS build failed - attempting manual copy"[0m
2025-10-16T08:03:55.6331322Z meson.build:1:0: ERROR: Unknown options: "harfbuzz, libtool"
2025-10-16T08:01:41.1345649Z [36;1m  echo "⚠️ Parallel build failed, trying single-threaded..."[0m
```

**📋 Context (100 dòng cuối log):**
```
2025-10-16T08:03:30.3771141Z   CC       silk/fixed/noise_shape_analysis_FIX.lo
2025-10-16T08:03:30.3786097Z   CC       silk/fixed/process_gains_FIX.lo
2025-10-16T08:03:30.4334527Z   CC       silk/fixed/regularize_correlations_FIX.lo
2025-10-16T08:03:30.4703694Z   CC       silk/fixed/residual_energy16_FIX.lo
2025-10-16T08:03:30.4972924Z   CC       silk/fixed/residual_energy_FIX.lo
2025-10-16T08:03:30.5387558Z   CC       silk/fixed/warped_autocorrelation_FIX.lo
2025-10-16T08:03:30.5674664Z   CC       silk/fixed/apply_sine_window_FIX.lo
2025-10-16T08:03:30.5865402Z   CC       silk/fixed/autocorr_FIX.lo
2025-10-16T08:03:30.6070888Z   CC       silk/fixed/burg_modified_FIX.lo
2025-10-16T08:03:30.6546419Z   CC       silk/fixed/k2a_FIX.lo
2025-10-16T08:03:30.6724009Z   CC       silk/fixed/k2a_Q16_FIX.lo
2025-10-16T08:03:30.6831565Z   CC       silk/fixed/pitch_analysis_core_FIX.lo
2025-10-16T08:03:30.7586357Z   CC       silk/fixed/vector_ops_FIX.lo
2025-10-16T08:03:30.7730603Z   CC       silk/fixed/schur64_FIX.lo
2025-10-16T08:03:30.7949641Z   CC       silk/fixed/schur_FIX.lo
2025-10-16T08:03:30.8719257Z   CC       src/opus.lo
2025-10-16T08:03:30.8897359Z   CC       src/opus_decoder.lo
2025-10-16T08:03:30.9103957Z   CC       src/opus_encoder.lo
2025-10-16T08:03:30.9164059Z   CC       src/extensions.lo
2025-10-16T08:03:31.0061903Z src/extensions.c:504:18: warning: variable 'trailing_short_len' set but not used [-Wunused-but-set-variable]
2025-10-16T08:03:31.0062832Z       opus_int32 trailing_short_len;
2025-10-16T08:03:31.0253600Z                  ^
2025-10-16T08:03:31.0254011Z   CC       src/opus_multistream.lo
2025-10-16T08:03:31.1051336Z 1 warning generated.
2025-10-16T08:03:31.1165978Z   CC       src/opus_multistream_encoder.lo
2025-10-16T08:03:31.1409418Z   CC       src/opus_multistream_decoder.lo
2025-10-16T08:03:31.1419155Z   CC       src/repacketizer.lo
2025-10-16T08:03:31.3165152Z   CC       src/opus_projection_encoder.lo
2025-10-16T08:03:31.3173244Z   CC       src/opus_projection_decoder.lo
2025-10-16T08:03:31.3881906Z   CC       src/mapping_matrix.lo
2025-10-16T08:03:31.3939633Z   CC       src/analysis.lo
2025-10-16T08:03:31.4431981Z   CC       src/mlp.lo
2025-10-16T08:03:31.4599819Z   CC       src/mlp_data.lo
2025-10-16T08:03:31.5341285Z   CPPAS    celt/arm/celt_pitch_xcorr_arm-gnu.lo
2025-10-16T08:03:31.6002482Z   CCLD     libarmasm.la
2025-10-16T08:03:31.6848789Z   CCLD     libopus.la
2025-10-16T08:03:32.4042659Z make[2]: Leaving directory '/home/runner/work/113/113/external/opus'
2025-10-16T08:03:32.4048468Z make[1]: Leaving directory '/home/runner/work/113/113/external/opus'
2025-10-16T08:03:32.4460267Z make  install-recursive
2025-10-16T08:03:32.4754732Z make[1]: Entering directory '/home/runner/work/113/113/external/opus'
2025-10-16T08:03:32.5187763Z make[2]: Entering directory '/home/runner/work/113/113/external/opus'
2025-10-16T08:03:32.5452669Z make[3]: Entering directory '/home/runner/work/113/113/external/opus/doc'
2025-10-16T08:03:32.5453325Z make[3]: Nothing to be done for 'all'.
2025-10-16T08:03:32.5453697Z make[3]: Leaving directory '/home/runner/work/113/113/external/opus/doc'
2025-10-16T08:03:32.5747605Z make[3]: Entering directory '/home/runner/work/113/113/external/opus'
2025-10-16T08:03:32.6007897Z  /usr/bin/mkdir -p '/home/runner/work/113/113/external/../build/external/share/aclocal'
2025-10-16T08:03:32.6012581Z  /usr/bin/mkdir -p '/home/runner/work/113/113/external/../build/external/lib/pkgconfig'
2025-10-16T08:03:32.6015836Z  /usr/bin/mkdir -p '/home/runner/work/113/113/external/../build/external/include/opus'
2025-10-16T08:03:32.6016727Z make[4]: Entering directory '/home/runner/work/113/113/external/opus/doc'
2025-10-16T08:03:32.6053830Z  /usr/bin/install -c -m 644 opus.pc '/home/runner/work/113/113/external/../build/external/lib/pkgconfig'
```

**🔍 Nguyên nhân gốc rễ:**
- [ ] TODO: Cần phân tích thủ công
- Loại lỗi: Unknown

**🛠️ Fix đã thử:**
- [ ] TODO: Cập nhật sau khi thử fix

**📝 Status:** 🔴 Chưa fix

**🏷️ Tags:** `Unknown` `auto-generated` `run-4`

---

