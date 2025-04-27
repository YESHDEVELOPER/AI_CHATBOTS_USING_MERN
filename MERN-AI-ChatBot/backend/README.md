
# MERN Stack AI Chatbot

This is an AI Chatbot application, inspired by ChatGPT, by using MERN Stack and OpenAI

It's a customized chatbot where each message of the user is stored in DB and can be retrieved and deleted.

It's a completely secure application using JWT Tokens, HTTP-Only Cookies, Signed Cookies, Password Encryption, and Middleware Chains.

Of course! Here's your content made more **professional**, **organized**, and **attractive** — with **emojis**, **logos**, and some **formatting improvements**.  
(For logos, since you can't directly render images in markdown without hosting, I added beautiful Unicode and emoji icons.)

---

# 🚀 **Project Overview: AI Chatbot with MERN Stack & GPT-3.5**

The project is a **💬 Chatbot** developed using the powerful **MERN** stack (**MongoDB**, **Express**, **React**, **Node.js**).  
The **backend** handles user authentication, conversation saving, and integrates **OpenAI's GPT-3.5 API** to generate smart responses.

---

# 🛠️ **Key Backend Components**

## 1. 🔒 User Authentication & Authorization
- **User Signup** (`userSignup`) ➡️ Register users with name, email, and password (hashed for security 🔐).
- **User Login** (`userLogin`) ➡️ Authenticate and issue **JWT** tokens stored in HTTP-only cookies.
- **User Logout** (`userLogout`) ➡️ Clear JWT cookie to safely log out.
- **Verify User** (`verifyUser`) ➡️ Ensure only authenticated users access protected routes.

## 2. 💬 Chatbot Conversations
- **Store Chats** ➡️ Save conversation history in MongoDB.
- **Retrieve Chats** ➡️ Fetch all past conversations.
- **Delete Chats** ➡️ Erase entire chat history.
- **Generate Chat Responses** ➡️ Integrate with **OpenAI GPT-3.5** for intelligent replies.

## 3. 🔗 OpenAI API Integration
- Seamless connection with **OpenAI** to maintain context-aware conversations.
- API key and organization ID secured in `.env` files.

## 4. 🗄️ Database (MongoDB)
- **User Model** ➡️ Stores `name`, `email`, `password`, and `chats`.
- Efficient storage and retrieval of chat data using **Mongoose**.

## 5. ⚙️ Middlewares
- **JWT Verification** ➡️ Validates tokens for protected endpoints.
- **Request Validation** ➡️ Ensures clean and safe inputs using `express-validator`.

## 6. 🛤️ Routing Structure
- **User Routes** ➡️ `/signup`, `/login`, `/logout`, `/auth-status`
- **Chat Routes** ➡️ `/new`, `/all-chats`, `/delete`

## 7. 🛡️ Error Handling and Logging
- Standardized error handling with **try-catch** blocks.
- Server activity monitored using **Morgan Logger**.

---

# 🔄 **Application Flow**

## 1️⃣ User Registration
- ➡️ Frontend sends user data ➡️ Backend encrypts password ➡️ Saves user ➡️ Issues JWT Token.

## 2️⃣ User Login
- ➡️ Validate credentials ➡️ Create new JWT Token ➡️ Save in secure cookie.

## 3️⃣ Chat Interaction
- ➡️ Authenticated user sends a message ➡️ Backend interacts with OpenAI ➡️ Saves response ➡️ Sends updated chat.

## 4️⃣ Retrieve & Delete History
- ➡️ `/all-chats` to retrieve all conversations.
- ➡️ `/delete` to clear entire chat history.

---

# 🧩 **Tech Stack**
| Technology | Purpose |
| :--- | :--- |
| **Node.js** 🟩 | Backend runtime |
| **Express.js** ⚡ | Routing and server |
| **MongoDB** 🍃 | NoSQL database |
| **Mongoose** | MongoDB ORM |
| **JWT** 🔑 | Secure authentication |
| **Bcrypt** 🔒 | Password hashing |
| **OpenAI API** 🤖 | Chatbot intelligence |
| **dotenv** 📄 | Manage secrets |
| **Cors** 🌐 | Cross-origin resource sharing |

---

# 🔐 **Security Features**
- **Password Hashing** with `bcrypt`.
- **JWT Authentication** for stateless, secure logins.
- **HTTP-Only Cookies** to prevent XSS attacks.
- **Input Validation** to block malicious payloads.

---

# 🔥 **Future Improvements**
- ✨ Add **User Profiles** and preferences.
- ✨ **Optimize Chat History** to maintain efficient API payloads.
- ✨ Implement **Centralized Error Handling**.
- ✨ Introduce **Rate Limiting** to prevent server abuse.

---

# 📈 **Detailed Flow Examples**

## 1. 👤 User Signup
```javascript
axios.post('/api/v1/signup', {
  name: 'John Doe',
  email: 'john@example.com',
  password: 'securePass123'
});
```
✅ Backend encrypts the password, stores the user, and returns a **JWT token**.

---

## 2. 🔐 User Login
```javascript
axios.post('/api/v1/login', {
  email: 'john@example.com',
  password: 'securePass123'
});
```
✅ Backend verifies credentials and issues a **secure cookie** with the token.

---

## 3. 🛡️ Sending Authenticated Requests
```javascript
axios.post('/api/v1/new', 
  { message: 'Hello, bot!' }, 
  { headers: { 'Authorization': `Bearer ${getCookie('auth_token')}` } }
);
```
✅ Only verified users can access protected routes.

---

# 🗣️ **Chat Message Flow**
1. User sends message via frontend ➡️
2. Backend adds it to conversation history ➡️
3. Posts updated conversation to **OpenAI GPT-3.5** ➡️
4. Appends and stores the AI's response ➡️
5. Sends updated chat back to frontend.

---

# 📚 **Conclusion**

This **AI Chatbot** project elegantly combines **authentication**, **chat history management**, and **OpenAI GPT-3.5 intelligence** into a **secure, scalable** MERN application.  
🔗 Focused on **real-world conversation flows**, **security best practices**, and **scalable architecture**.

---

---

