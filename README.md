# how-to-connect-h100



---

### ✅ 解法 A：切換到乾淨目錄下建置

建議你把 `Dockerfile.txt` 和相關檔案（如程式碼、模型等）放在一個乾淨資料夾內，然後在那裡執行 build：

```bash
mkdir ~/docker_build_test
cp Dockerfile.txt ~/docker_build_test/
cd ~/docker_build_test
docker build -f Dockerfile.txt -t myimage:latest .
```
