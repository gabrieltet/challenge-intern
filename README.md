# Data manipulation
In this challenge you will code a set of methods to manipulate a set of data based on some input.

This data represents the output of a query and describes the scores of a student enrolled in many courses. Based on the structure presented, you will provide some mathods to query and mutate the given data.

# Definitions

A *student* is defined by it's id and a name. Duplicated names are allowed.
```json
{"id": 1, "name": "Andy Warhol"}
{"id": 2, "name": "Yayoi Kusama"}
```

A *course* is defined by it's id and a name. Duplicated names are **not** allowed.
```json
{"id": 1, "name": "Fine Arts"}
{"id": 2, "name": "Musical Theory"}
```

An *assessment* is described by the relation of a *student* and a *course* through their id's and a score. A student may have more than one score for the same course. The score field is typed as string and might have values from zero to 10.0.
```json
{"id": 1, "student_id": 1, "course_id": 2, "score": "7.5"}
```

# Requirements

You need to provide a set of functions to query and mutate not only the provided data but any given data set. Name your functions according to the ones in the examples. You are free to create any other function if needed.

## Queries
 * Get a list containing the **names** of all enrolled students in an course.
 ```javascript
 getEnrolledStudents(course_id)
 // Output: ["John Smith", "Mary Adams"]
 ```
 * Get the final score of a student in a course. The final score of a student in a course is the sum of all student's scores in that course. The maximum final score is 10.0. Anything higher than that number should be returned as "10.0".
 ```javascript
 getFinalScore(student_id, course_id)
 // Output: "8.5"
 ```
  * Given a course id and a tuple describing a range of scores, get a list containing the **names** of all enrolled students in that course with final scores within that range. 
 ```javascript
 [min_score, max_score]
 ```
 ```javascript
 getStudentsNamesByScoreRange(range, course_id)
 // Inputs: ["7.0", "9.0"], 2
 // Output: ["John Lennon", "Paul McCartney", "Ringo Starr", "George Harrison"]
 ```
 
 ## Mutations
 * Given an Array-like query, add a new score to the user in a course. The query also requires a boolean type field which describes if the system should delete all previous scores for that user in that course if true. This function outputs the new final score of that user. (Hint: use your previous functions)
 ```javascript
 [user_id, course_id, score, should_delete_all_scores]
 ```
 ```javascript
 addScoreToUserInCourse(query)
 // Input: [2, 2, "5.0", true]
 // Output: "5.0"
 ```
 
 # About the challenge
  * You are free to choose any programming language for this implementation
  * Write all code and documentation in english
  * Provide a README containing installation instructions
  
Please fork this repository and send us the link with your solution. If you don't want to have this repository in your profiles, feel free to use another git solution like GitLab or send us a git patch file.

Feel free to contact us if you have any questions.
