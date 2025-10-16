# 📚 FFmpeg Android ARM32 - Error Knowledge Base

> **Mục đích:** Tự động ghi lại toàn bộ lỗi build để tránh lặp lại sai lầm
> 
> **Cập nhật:** Tự động bởi GitHub Actions
> 
> **Tổng số lỗi:** 

---

## 📋 Quick Reference

| ID | Tên lỗi | Tần suất | Workflow | Ngày |
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

