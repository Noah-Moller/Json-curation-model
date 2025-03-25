# JSON Curation Model

The **JSON Curation Model (JCM)** is the first model in the **Tetrix Context Architecture**. Its primary purpose is to curate JSON entries based on **contextual relevance**.

### Example Use Case

Say you have a JSON object like this:

```json
{
  "id": 101,
  "name": "Alex Morgan",
  "email": "alex.morgan@example.com",
  "isActive": true,
  "createdAt": "2025-03-23T15:30:00Z",
  "profile": {
    "age": 29,
    "gender": "male",
    "location": {
      "city": "San Francisco",
      "state": "CA",
      "country": "USA"
    },
    "interests": ["coding", "photography", "travel"]
  },
  "settings": {
    "theme": "dark",
    "notifications": {
      "email": true,
      "sms": false,
      "push": true
    }
  }
}
```

A lot of these fields aren’t relevant for our use case. For example, we might not need the `id`, `createdAt`, or any of the `settings` information.

The JCM filters this down to only the **essential** data:

```json
{
  "name": "Alex Morgan",
  "email": "alex.morgan@example.com",
  "isActive": true,
  "profile": {
    "age": 29,
    "gender": "male",
    "location": {
      "city": "San Francisco",
      "state": "CA",
      "country": "USA"
    },
    "interests": ["coding", "photography", "travel"]
  }
}
```

This is **much cleaner** and easier to process, as we’re now only working with the **contextually relevant information**.

