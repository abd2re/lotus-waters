# API Documentation

## **Base URL**

`http://<your_server_address>`

---

## **Models**

### **1. Character**

Represents a character in a story.

```json
{
  "name": "str",
  "description": "str"
}
```

### **2. Scene**

Represents a scene within a story.

```json
{
  "sequence_number": "int",
  "content": "str",
  "image_url": "str",
  "audio_url": "str"
}
```

### **3. Story**

Represents the main story object.

```json
{
  "id": "int",
  "content": "str",
  "scenes": "list[Scene]",
  "completion": "int",
  "characters": "list[Character]",
  "cover_image_url": "str"
}
```

---

## **Endpoints**

### **1. GET /get_story**

Retrieve the details of a story by its ID.

#### **Request Parameters**

- `id` (int, required): The ID of the story.

#### **Database Interaction**

- **Read:** Fetches the story with the specified `id` from the `stories_collection`.

#### **Response**

- Returns a `Story` object.

#### **Example**

```json
GET /get_story?id=1
Response:
{
  "id": 1,
  "content": "Once upon a time...",
  "scenes": [],
  "completion": 0,
  "characters": [],
  "cover_image_url": "None"
}
```

---

### **2. POST /initialize_story**

Initialize a new story with a given ID.

#### **Request Body**

- `id` (int, required): The ID of the story to initialize.

#### **Database Interaction**

- **Write:** Inserts a new `Story` object into the `stories_collection` with the provided `id`.

#### **Response**

- Returns the initialized `Story` object.

#### **Example**

```json
POST /initialize_story
Body:
{
  "id": 1
}
Response:
{
  "id": 1,
  "content": "",
  "scenes": [],
  "completion": 0,
  "characters": [],
  "cover_image_url": "None"
}
```

---

### **3. GET /character_question_options**

Generate character-related question options for a story.

#### **Request Parameters**

- `story_id` (int, required): The ID of the story.
- `question` (str, required): The question for generating options.

#### **Database Interaction**

- **Read:** Fetches the story with the specified `story_id` from the `stories_collection`.

#### **Response**

- Returns a dictionary with three options:
    - `option1` (str)
    - `option2` (str)
    - `option3` (str)

#### **Example**

```json
GET /character_question_options?story_id=1&question="What is the character's role?"
Response:
{
  "option1": "Hero",
  "option2": "Villain",
  "option3": "Mentor"
}
```

---

### **4. POST /character_add_answer**

Add a response to a character-related question and update the story.

#### **Request Body**

- `story_id` (int, required): The ID of the story.
- `response` (str, required): The user's response to the question.

#### **Database Interaction**

- **Read:** Fetches the story with the specified `story_id` from the `stories_collection`.
- **Write:** Updates the `content` and `characters` fields of the story in the `stories_collection`.

#### **Response**

- Returns `None`. The story is updated in the database.

#### **Example**

```json
POST /character_add_answer
Body:
{
  "story_id": 1,
  "response": "The hero is brave and determined."
}
```

---

### **5. POST /create_scene**

Create a new scene in the story based on user input.

#### **Request Body**

- `story_id` (int, required): The ID of the story.
- `response` (str, required): Input to generate the scene.

#### **Database Interaction**

- **Read:** Fetches the story with the specified `story_id` from the `stories_collection`.
- **Write:** Updates the `scenes`, `content`, and `characters` fields of the story in the `stories_collection`.

#### **Response**

- Returns a dictionary with the new scene's details:
    - `content` (str)
    - `image_url` (str)

#### **Example**

```json
POST /create_scene
Body:
{
  "story_id": 1,
  "response": "A forest filled with magical creatures."
}
Response:
{
  "content": "The forest was alive with magical creatures.",
  "image_url": "http://example.com/image.png"
}
```

---

### **6. GET /get_options**

Retrieve story progression options based on completion percentage.

#### **Request Parameters**

- `story_id` (int, required): The ID of the story.
- `completion` (int, required): The current completion percentage of the story.

#### **Database Interaction**

- **Read:** Fetches the story with the specified `story_id` from the `stories_collection`.
- **Write:** Updates the `completion` field of the story in the `stories_collection`.

#### **Response**

- Returns a dictionary with three options:
    - `option1` (str)
    - `option2` (str)

#### **Example**

```json
GET /get_options?story_id=1&completion=50
Response:
{
  "option1": "Introduce a new character.",
  "option2": "Reveal a hidden truth.",
}
```

---

## **Database Interaction Summary**

- **Read Operations**:
    
    - `/get_story`
    - `/character_question_options`
    - `/create_scene`
    - `/get_options`
- **Write Operations**:
    
    - `/initialize_story`: Inserts a new story.
    - `/character_add_answer`: Updates the `content` and `characters` of a story.
    - `/create_scene`: Updates the `scenes`, `content`, and `characters` of a story.
    - `/get_options`: Updates the `completion` of a story.
