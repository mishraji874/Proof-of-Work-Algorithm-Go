# ⛏️ Build Your Own Blockchain with Proof-of-Work in Go

**A fun and educational project that walks you through building your own blockchain in under 200 lines of Go code — complete with mining and Proof-of-Work!**
**Learn how Bitcoin-like consensus mechanisms work, one hash at a time.**

---

## 📜 Overview

Ever wondered how Bitcoin or Ethereum mining actually works? 🤔
This project demystifies the concept by walking you through creating a **mini blockchain** from scratch using **Go** — complete with a REST API and **Proof-of-Work** mining!

By the end, you’ll understand:
- 🧠 What mining really means (hint: not just “solving a math problem”)
- 🔐 How cryptographic hashing powers blockchain consensus
- 🧱 How to create and validate blocks
- 🚀 How to build and test your own mining logic

---

## 🏗️ Project Architecture

- All logic is contained in a single `main.go` file.
- REST API with two routes:
  - `GET /` - View current blockchain
  - `POST /` - Add a new block with your BPM (pulse rate)
- Uses SHA-256 hashing with Proof-of-Work for block validation.
- Difficulty level is configurable (starts with 1 leading zero).
- Includes mutex locks to avoid race conditions when mining.

---

## 🛠️ Tech Stack

- Language: **Go**
- Libraries:
  - [`gorilla/mux`](https://github.com/gorilla/mux) - HTTP routing
  - [`davecgh/go-spew`](https://github.com/davecgh/go-spew) - Pretty printing structs
  - [`joho/godotenv`](https://github.com/joho/godotenv) - Environment variable loader

---

## 📦 Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone https://github.com/mishraji874/Proof-of-Work-Algorithm-Go.git
   cd Proof-of-Work-Algorithm-Go
   ```

2. **Install Dependencies**
  ```bash
    go get github.com/gorilla/mux
    go get github.com/davecgh/go-spew/spew
    go get github.com/joho/godotenv
  ```

3. **Create `.env` file**
  ```env
  ADDR=8080
  ```

4. **Run the App**
  ```bash
  go run main.go
  ```

5. **Test in Your Browser**
Open `http://localhost:8080` to view your blockchain.

6. **Add a Block with Postman or curl**

POST to `http://localhost:8080` with JSON body:

```json
{ "BPM": 72 }
```

## 🧪 How Mining Works

Each block is only added when:
- Its hash starts with a defined number of leading zeros (`difficulty`)
- Proof-of-Work loop finds the correct `Nonce` to satisfy this condition

✅ You’ll see the mining process in real-time with the terminal output!

## 🔐 Core Concepts Covered

- Blockchain structure (Genesis block, previous hashes)
- SHA-256 hashing
- Nonce and Proof-of-Work mining
- Blockchain immutability
- RESTful web server with Go
- Data races & mutex locking

## 🚀 Live Demo

- Start the server: `go run main.go`
- Visit: `http://localhost:8080`
- POST with:

  ```bash
  curl -X POST -H "Content-Type: application/json" -d '{"BPM": 65}' http://localhost:8080
  ```

Watch your terminal as the mining happens in real-time!

## 🤝 Contributing

Pull requests are welcome! Feel free to fork the repo and suggest improvements, feature additions, or even upgrades to the Proof-of-Work mechanism.

## 📬 Contact
For any inquiries or support, reach out via:

🌐 Portfolio: https://adityamishra-dev.vercel.app/

🐦 Twitter: https://x.com/mishraji874_eth

🔗 LinkedIn: https://www.linkedin.com/in/aditya-mishra-a76237226/
