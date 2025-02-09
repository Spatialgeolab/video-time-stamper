# 畫布 (Canvas) 工具 README

這是一個提供自訂繪圖與錄製功能的前端工具，主要透過 HTML 的 `<canvas>` 元素在瀏覽器端進行繪製。你可以在此畫布上進行手繪、載入圖片、疊加文字或其他視覺效果，也可以透過 `canvas.captureStream()` 與 `MediaRecorder` 實現錄製、下載等應用。

## 功能概要

1. **自訂繪圖**
   - 在畫布上任意繪製線條、圖形、文字，或載入圖片等。
2. **錄製與下載**
   - 使用 `canvas.captureStream()` 搭配 `MediaRecorder`，可將繪製過程錄製為影片，並輸出成 WebM 等格式。
3. **動態效果**
   - 透過 JavaScript 進行動畫，搭配 `requestAnimationFrame` 或 `setInterval` 更新畫布內容。
4. **可調整參數**
   - 使用者可自訂畫布尺寸、FPS、碼率、輸出格式等。

## 注意事項

1. **瀏覽器支援**
   - `MediaRecorder` 與 `canvas.captureStream()` 在各瀏覽器支援度有所差異，建議使用新版 Chrome、Firefox 或 Safari。
2. **效能**
   - 如果畫布更新頻率高、解析度高、或碼率設定過高，可能造成 CPU/GPU 壓力大，導致掉幀或錄製不順。
3. **編碼格式**
   - 多數瀏覽器對 `video/webm;codecs=vp9` 的支援較好，若需要 MP4 等格式，要視瀏覽器支援或進行後端轉檔。
4. **儲存繪製內容**
   - 若需存儲或恢復繪圖狀態，需自行維護繪圖指令序列或使用圖片快照。

