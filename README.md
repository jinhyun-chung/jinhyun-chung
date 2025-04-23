# 📊 ERD (Entity-Relationship Diagram)

이 문서는 프로젝트의 데이터베이스 구조를 이해하기 위한 ERD(Entity-Relationship Diagram)를 설명합니다.

## 📌 개요

ERD는 데이터베이스에 어떤 **데이터(엔티티)** 가 저장되며, 이들 간에 어떤 **관계(Relationship)** 가 있는지를 시각적으로 표현한 도구입니다.

---

## 🧱 주요 엔티티

### 1. 🧍‍♂️ User (회원)
- `id`: 사용자 고유 ID (PK)
- `name`: 이름
- `email`: 이메일 주소
- `password`: 비밀번호 (암호화 저장)

### 2. 📦 Product (상품)
- `id`: 상품 고유 ID (PK)
- `name`: 상품명
- `description`: 설명
- `price`: 가격
- `stock`: 재고 수량

### 3. 🧾 Order (주문)
- `id`: 주문 고유 ID (PK)
- `user_id`: 주문한 사용자 ID (FK)
- `created_at`: 주문 일시

### 4. 📋 OrderItem (주문 항목)
- `id`: 항목 고유 ID (PK)
- `order_id`: 주문 ID (FK)
- `product_id`: 상품 ID (FK)
- `quantity`: 수량
- `price`: 단가

---

## 🔗 엔티티 관계

- 하나의 **User**는 여러 개의 **Order**를 가질 수 있습니다. (1:N)
- 하나의 **Order**는 여러 개의 **OrderItem**을 포함합니다. (1:N)
- 하나의 **Product**는 여러 **OrderItem**에 포함될 수 있습니다. (1:N)

---

## 📷 ERD 다이어그램

> 🔽 다이어그램은 아래와 같이 그릴 수 있습니다 (이미지를 삽입하거나 툴 링크):

![ERD Diagram](https://your-image-link.com/erd.png)  
_또는 [dbdiagram.io](https://dbdiagram.io) 와 같은 ERD 도구를 사용하여 시각화할 수 있습니다._

---

## 📚 참고

- ERD 툴 추천: [dbdiagram.io](https://dbdiagram.io), [draw.io](https://app.diagrams.net), [Lucidchart](https://www.lucidchart.com)
- 마크다운 이미지 삽입법: `![설명](이미지 링크)`
