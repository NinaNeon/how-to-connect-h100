# how-to-connect-h100

https://afspod-docs.dginfra.gov.tw/s/container-image

---

### ✅ 解法 A：切換到乾淨目錄下建置

建議你把 `Dockerfile.txt` 和相關檔案（如程式碼、模型等）放在一個乾淨資料夾內，然後在那裡執行 build：

```bash
mkdir ~/docker_build_test
cp Dockerfile.txt ~/docker_build_test/
cd ~/docker_build_test
docker build -f Dockerfile.txt -t myimage:latest .
```
```bash
nina@nina-X550VX:~/docker_build_test$ docker login afspod-registry.dginfra.gov.tw
Username: p83254319.1
Password: 
WARNING! Your password will be stored unencrypted in /home/nina/.docker/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credential-stores

Login Succeeded
```


### ✅ 正確可執行版本：

```bash
docker tag myimage:latest afspod-registry.dginfra.gov.tw/dfc9a9be-007b-4d52-8f3c-8d2d1569eac3/myimage:latest

docker push afspod-registry.dginfra.gov.tw/dfc9a9be-007b-4d52-8f3c-8d2d1569eac3/myimage:latest
```

![image](https://github.com/user-attachments/assets/90c8c378-a2f2-41c1-a12c-7b1b12bdb466)

![image](https://github.com/user-attachments/assets/05c869fd-0346-4137-a0cc-e42f3ed2d9db)

![image](https://github.com/user-attachments/assets/6cf93f72-7c0f-4a8f-b1f6-7a06f0bc2ce4)

