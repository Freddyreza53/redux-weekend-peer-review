# Weekend Challenge 11 - React-Redux Feedback Form

## Instructions

Reviewing code is an important role developers play. We're going to practice reviewing code from others.

- Get the repo url from your partner
- Get your partner's project running on your computer
- Review the code from your partner and give relevant feedback
- Complete the Markdown section and submit that in the notes section on the assignment app. (Make sure you include who's code you reviewed.)

Practicing compassionate code reviews is important (you can learn more from this video on the topic: https://www.youtube.com/watch?v=Ea8EiIPZvh0 )

## Review Checklist

## Base Required Features 

- Multi-Part Form:  
  - [x] Able to add feedback
    - [x] Data collected on individual pages & components
    - [x] Click on next takes you to the next page in sequence
    - [x] Data saves in DB after *all* the parts are completed (not piecemeal)
    - [x] Thank you page takes you back to the first view
    - [x] Old Data is cleared on form completion

- Client code:
  - [x]  Individual components for each form part
  - [x]  Redux setup complete
    - [x] Store linked to react with `<Provider>`
    - [x] Store setup with reducer(s) and logger middleware 
  - [x] Reducers & Actions Working
    - [x] Actions are in SCREAMING_SNAKE_CASE and semantically named
    - [x] Actions have a `type` key, and `payload` if sending data
    - [x] Reducers are returning a new state, or the old state (not mutating)
    - [x] Reducers are using spread correctly (to keep old data, while adding new)
  - [x] Review Component shows at all times with current redux state
  - [x] React-Redux Working
    - [x] Dispatching actions onClick
    - [x] Grabbing data from the redux store with `useSelector`
  - [x] Axios POST request to add feedback


- Server code:   
  - [x] Router made for GET, POST


## General Items
Feedback should be provided for these items, but they do not impact scoring.

- Git 
  - [x] Multiple git commits showing incremental progress
  - [x] Commits are descriptive of the changes made or feature added 
  - [x] Has .gitignore with node_modules
  - [ ] Readme file updated (assuming this is previously discussed)
- Code Style 
  - [ ] Appropriate amount of code comments
  - [x] Code is consistently formatted
- Client
  - [x] Appropriate use of HTML tags
  - [x] Basic CSS styling with margins/padding


## Stretch Goals
First must be complete for score of  _Exceeds Expectations_

- Previous Steps
  - [x] allows a user to go to a previous step, either directly or by cycling backward thru the steps
  - [ ] user can update their score for a step
    - [ ] new score is validated to not be empty
    - [ ] redux is updated with new score
    - [ ] user can continue on to review page and submit as in Base Mode


- Admin View
  - [ ] All entries are visible with correct data from inputs
    - [ ] Most recent is at the top
  - [ ] Can Delete an entry
    - [ ] User is prompted before deleting
  - [ ] Axios GET request to get all feedback for `/admin` view in componentDidMount

  Busywork Goals, consider removing or making more useful

- [x] Styling with Material UI
- [ ] Ability to flag a feedback item on `/admin` for further review
- [ ] Deployed to Heroku


## Markdown

```
Hey Lucas ,

General Feedback.

---
| Functional Requirements | Complete? Yes |
| --- | :---: |
| Multi page form with client side routing and navigation (next button) | yes |
| Data stored in Redux when navigating from page to page | yes |
| User is notified when trying to leave a blank score | no, can't leave blank with slider |
| Review Component displays scores and comments from current redux state | yes |
| Submit button sends data to the server via Axios | yes |
| Confirmaion Page displays after data is POSTed to the server | yes |
| Button on Confirmation Page clears Redux and starts a new survey | no |
| Views are broken down into components | yes |

---
### Notes:

Notes on the above Functional Requirements.

---
| General Items | Complete? yes|
| --- | :---: |
| More than 15 git commits | no |
| Commits are descriptive of the changes made or feature added | yes |
| Readme file updated | no |
| Appropriate amount of code comments | no |
| Code is consistently formatted | yes |
| Server code organized with router & module files | yes |

---
### Notes:

Notes on General Items

Great job with slider! Also, nice work on storing all the feedback data on one reducer, one thing that I noticed is that redux isn't cleared after the user submits their form. This could be done with a dispatch action in the .then of the POST. Another tip, you should move your history.push's in the .then of the POST as well. That way if there is any errors in the catch, it won't clear and move to the next page. Besides that, everything looks good. Keep it up!

```
