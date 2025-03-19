# MongoDB schema first draft

### **1. Users Collection**

This collection stores user accounts, authentication details, and their conversations.

```javascript
{
  "_id": ObjectId("unique_user_id"),
  "name": "John Doe",
  "email": "johndoe@example.com",
  "password_hash": "hashed_password",
  "role": "paid",  // ["free", "paid", "admin"]
  "created_at": ISODate("2025-03-19T00:00:00Z"),
  "updated_at": ISODate("2025-03-19T00:00:00Z"),
  "conversations": [ObjectId("unique_conversation_id")],
  "oauth": {
    "provider": "google",
    "provider_user_id": "google_unique_id"
  },
  "2fa_enabled": true
}
```

---

### **2. Conversations Collection**

Stores all conversations between users and AI characters.

```javascript
{
  "_id": ObjectId("unique_conversation_id"),
  "user_id": ObjectId("unique_user_id"),
  "character_id": ObjectId("unique_character_id"),
  "created_at": ISODate("2025-03-19T00:00:00Z"),
  "updated_at": ISODate("2025-03-19T00:05:00Z"),
  "messages": [
    {
      "sender": "user",
      "message": "Hello, Batman!",
      "timestamp": ISODate("2025-03-19T00:01:00Z")
    },
    {
      "sender": "ai",
      "message": "Hello, how can I assist you today?",
      "timestamp": ISODate("2025-03-19T00:01:10Z")
    }
  ]
}
```

---

### **3. AI Characters Collection**

Stores available AI personalities and their characteristics.

```javascript
{
  "_id": ObjectId("unique_character_id"),
  "name": "Batman",
  "description": "A brooding vigilante of Gotham City.",
  "personality": {
    "traits": ["serious", "determined", "dark"],
    "knowledge_base": ["crime-fighting", "Gotham", "justice"]
  },
  "ai_settings": {
    "temperature": 0.7,
    "max_tokens": 500
  },
  "created_at": ISODate("2025-03-19T00:00:00Z"),
  "updated_at": ISODate("2025-03-19T00:00:00Z")
}
```

---

### **4. OAuth Accounts Collection**

Stores third-party authentication details.

```javascript
{
  "_id": ObjectId("unique_oauth_id"),
  "user_id": ObjectId("unique_user_id"),
  "provider": "google",
  "provider_user_id": "google_unique_id",
  "access_token": "encrypted_access_token",
  "refresh_token": "encrypted_refresh_token",
  "expires_at": ISODate("2025-03-19T01:00:00Z")
}
```

---

### **5. Password Reset Collection**

Handles password reset requests.

```javascript
{
  "_id": ObjectId("unique_reset_id"),
  "email": "johndoe@example.com",
  "token": "secure_reset_token",
  "expires_at": ISODate("2025-03-19T01:00:00Z")
}
```

---

### **6. Two-Factor Authentication (2FA) Collection**

Stores user 2FA settings.

```javascript
{
  "_id": ObjectId("unique_2fa_id"),
  "user_id": ObjectId("unique_user_id"),
  "secret": "generated_2fa_secret",
  "backup_codes": ["code1", "code2", "code3"],
  "created_at": ISODate("2025-03-19T00:00:00Z")
}
```

---

### **7. Account Deletion Requests**

Handles account deletion requests.

```javascript
{
  "_id": ObjectId("unique_deletion_id"),
  "user_email": "johndoe@example.com",
  "token": "secure_deletion_token",
  "token_expires_at": ISODate("2025-03-19T01:00:00Z")
}
```
