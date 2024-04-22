# Conversation Dataset Between Learners and AlgoBo

We share the conversation data collected in our prior studies. Each table represents a data point and its constituent information.

## [Student](https://github.com/TeachYou-org/conversation-data/blob/init/student.jsonl)

| Field     | Explanation                              | Example Value          |
|-----------|------------------------------------------|------------------------|
| id        | The unique identifier for each student   | "3V16YPm8ZjyRR5NdFZF8" |
| age       | The age of this student                  | 21                     |
| gender    | The gender of this student               | "female"               |
| degree    | The degree that this student is enrolled | "undergraduate"        |
| major     | The major of this student                | "computer science"     |
| ethnicity | The ethnicity of this student            | "Korean"               |

## [Session](https://github.com/TeachYou-org/conversation-data/blob/init/session.jsonl)

| Field             | Explanation                                                       | Example Value           |
|-------------------|-------------------------------------------------------------------|-------------------------|
| id                | The unique identifier for each message                            | "9EKWGHBUUX776htpMq9f"  |
| student_id        | The identifier of the student involved in this conversation       | "3V16YPm8ZjyRR5NdFZF8"  |
| created_at        | The timestamp in UTC of the first message                         | 1691325576331           |
| version           | The semantic version of AlgoBo regarding its prompting pipeline   | "1.0.1"                 |
| pre_test_id       | The identifier of test this student took before this conversation | "2lPrHoTj9jJM3bRtFW47"  |
| pre_test_response | The student’s response on the pre-test                            | "[\"O(log N)\", \"A\"]" |

## [Test](https://github.com/TeachYou-org/conversation-data/blob/init/test.jsonl)

| Field     | Explanation                                             | Example Value                                  |
|-----------|---------------------------------------------------------|------------------------------------------------|
| id        | The unique identifier for each set of test questions    | "2lPrHoTj9jJM3bRtFW47"                         |
| questions | An array of question identifiers that consist this test | "[\"1bgYkYReTO6FKuMg0\",\"1E06vSBOpFM7NX14\"]" |

## [Question](https://github.com/TeachYou-org/conversation-data/blob/init/question.jsonl)

| Field        | Explanation                                                  | Example Value                                   |
|--------------|--------------------------------------------------------------|-------------------------------------------------|
| id           | The unique identifier for each question                      | "1bgYkYReTO6FKuMg0"                             |
| type         | The type ("free-form" or "multiple-choice") of this question | "free-form"                                     |
| question     | The original content of this question                        | "이진 검색의 시간 복잡도는 얼마인가요?"                  |
| question_eng | The machine translated version of the question field         | "What is the time complexity of binary search?" |
| answer       | The answer of this question                                  | "O(log N)"                                      |
| answer_eng   | The machine translated version of the answer field           | "O(log N)"                                      |

## [Message](https://github.com/TeachYou-org/conversation-data/blob/init/message.jsonl)

| Field               | Explanation                                                    | Example Value                                                                                                                                             |
|---------------------|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| id                  | The unique identifier for each message                         | "15Cnx73Wa7Yv5hsi1pN0"                                                                                                                                    |
| created_at          | The timestamp in UTC that this message is sent to/by a student | 1691325576331                                                                                                                                             |
| session_id          | The identifier for the conversation that includes this message | "9EKWGHBUUX776htpMq9f"                                                                                                                                    |
| speaker             | The speaker ("student" or "algobo") of this message            | "student"                                                                                                                                                 |
| message             | The content of this message in its original language           | "배열의 양끝과 중간에 있는 데이터를 기준으로 절반식 나누어 가면서 탐색하면 가능해"                                                                                            |
| message_eng         | Machine translated version of the message field                | "You can search by dividing the array in half based on the data at both ends and the middle."                                                             |
| message_type        | Human-annotated instructional function of this message         | "Statement_Comprehension"                                                                                                                                 |
| message_quality     | Human-annotated quality of this message                        | "Vague"                                                                                                                                                   |
| knowledge_state     | The knowledge state of AlgoBo when this message is sent        | "[\"선형 검색은 배열의 각 요소를 두 부분으로 나누어 검색 범위를 좁혀가며 원하는 값을 찾는다\", \"배열 내 검색을 위해 while 문을 사용한다.\"]"                                          |
| knowledge_state_eng | Machine translated version of the knowledge_state field        | "[\"Linear search divides each element of an array into two parts and narrows the search range\", \"Use a while statement to search within the array.\"]" |
