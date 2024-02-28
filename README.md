# Self-hosted GitHub Action Runner on Docker

Containerized self-hosted GitHub Action Runner on Docker and Compose V2

## Prerequisites

1. Docker + Docker Compose V2
2. [PAT (Personal access token)](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens) for GitHub Account

## Steps

1. Copy .env.example to .env and fill out all variables with your
2. Create network
3. Run with Docker Compose

## Copy .env.example to .env and fill out all variables with your

```sh
mv .env.example .env

code .env
```

## Create Docker network

```sh
docker network create -d bridge net101
```

## Run with Docker Compose

```sh
docker compose build

docker compose up -d
```

## Remarks

- If the container is shutdown with graceful status, the runner will be removed from the GitHub repo automatically

## Reference

- [Create a Docker based Self Hosted GitHub runner Linux container](https://dev.to/pwd9000/create-a-docker-based-self-hosted-github-runner-linux-container-48dh)
- [How to containerize a GitHub Actions self-hosted runner](https://baccini-al.medium.com/how-to-containerize-a-github-actions-self-hosted-runner-5994cc08b9fb)

---

รัน GitHub Action Runner บน Container ด้วย Docker Compose V2

## สิ่งที่ต้องเตรียม

1. Docker + Docker Compose V2
2. [PAT (Personal access token)](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens) สำหรับ GitHub Account

## ขั้นตอน

1. สร้างไฟล์ .env จากตัวอย่างในไฟล์ .env.example และเติมค่า
2. สร้างเครือข่ายบน Docker
3. รันด้วย Docker Compose

## สร้างไฟล์ .env จากตัวอย่างในไฟล์ .env.example และเติมค่า

```sh
mv .env.example .env

code .env
```

## สร้างเครือข่ายบน Docker

```sh
docker network create -d bridge net101
```

## รันด้วย Docker Compose

```sh
docker compose build

docker compose up -d
```

## หมายเหตุ

- หากคอนเทนเนอร์ถูกปิดด้วยสถานะสมบูรณ์ ตัว runner จะถูกลบออกจาก GitHub repo โดยอัตโนมัติ

## อ้างอิง

- [Create a Docker based Self Hosted GitHub runner Linux container](https://dev.to/pwd9000/create-a-docker-based-self-hosted-github-runner-linux-container-48dh)
- [How to containerize a GitHub Actions self-hosted runner](https://baccini-al.medium.com/how-to-containerize-a-github-actions-self-hosted-runner-5994cc08b9fb)
