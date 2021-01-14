#### Function
````
/**
 * Inserts a comment into ...
    - "name", the name of the user posting the comment
    - "email", the email of the user posting the comment
    - "item_id", the _id of the movie pertaining to the comment
    - "text", the text of the comment
    - "date", the date when the comment was posted
 * @param {string} itemId - The _id of the item in e.g. database
 * @param {Object} user - An object containing the user's name and email.
 * @param {string} comment - The text of the comment.
 * @param {string} date - The date on which the comment was posted.
 * @returns {DAOResponse} Returns an object or "error"
*/
static async addComment(itemId, user, comment, date) {
    try {
    
        const commentDoc = { 
            'item_id': movieId, 
            'name': user.name, 
            'email': user.email,
            'text': comment,
            'date': date
        }
        
        // do something
        return await ... // e.g. insert comments to database
    } catch (e) {
        console.error(`Unable to post comment: ${e}`)
        return { error: e }
    }
}
````
