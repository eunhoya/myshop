MyShop - Next.js 쇼핑몰 프로젝트

📌 프로젝트 개요

MyShop은 Next.js 기반으로 개발된 쇼핑몰 프로젝트입니다. JWT 기반의 인증 시스템을 사용하며, MySQL과 Sequelize를 활용하여 백엔드 데이터 관리를 수행합니다.

🚀 프로젝트 설정 및 실행 방법

1️⃣ 프로젝트 클론 & 설치

# GitHub에서 프로젝트 클론

git clone https://github.com/your-username/myshop.git
cd myshop

# 패키지 설치

npm install

2️⃣ 환경 변수 설정

📌 프로젝트 루트에 .env.local 파일을 생성하고 아래 내용을 추가합니다.

DB_NAME=myshopDB
DB_USER=root
DB_PASS=your_password
DB_HOST=localhost
JWT_SECRET=your_secret_key

3️⃣ MySQL 데이터베이스 설정

MySQL에서 myshopDB 데이터베이스 생성

CREATE DATABASE myshopDB;

테이블 생성 (DBeaver 또는 MySQL Workbench에서 실행)

CREATE TABLE users (
id INT AUTO_INCREMENT PRIMARY KEY,
username VARCHAR(255) NOT NULL UNIQUE,
password VARCHAR(255) NOT NULL,
created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

4️⃣ Sequelize 설정 및 동기화

📌 myshop/lib/sequelize.js에서 데이터베이스 설정을 확인한 후, 동기화 실행

npm run dev

🔥 기능 목록

✅ 1. 사용자 인증 (JWT 기반)

회원가입 (/api/auth/signup)

로그인 (/api/auth/login)

현재 로그인한 사용자 정보 조회 (/api/auth/me)

✅ 2. 프론트엔드 상태 관리 (Zustand 사용)

Zustand를 활용한 로그인 상태 유지

로그인 후 JWT 저장 및 인증 유지

🛠 기술 스택

Frontend: Next.js, Zustand, Tailwind CSS

Backend: Next.js API Routes, Sequelize, MySQL

Auth: JWT (jsonwebtoken), bcryptjs

Deployment: Vercel (예정)

📌 Git & 버전 관리

# Git 초기화

git init

# GitHub 원격 저장소 연결

git remote add origin https://github.com/your-username/myshop.git

# 첫 커밋 및 푸시

git add .
git commit -m "Initial commit"
git branch -M main
git push -u origin main

🎯 앞으로의 개발 계획

🔹 상품 데이터 관리 및 CRUD 기능 추가

🔹 장바구니 및 결제 기능 구현

🔹 Vercel을 통한 배포 및 CI/CD 적용
