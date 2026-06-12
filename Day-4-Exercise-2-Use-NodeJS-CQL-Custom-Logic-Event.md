# Day 4 Exercise 2
This is a reference of Code for Day 4 Exercise 2

## Enhanced **submitOrder** custom event
### Steps
1. Open `srv/admin-custom-service.js` and modify the custom event `submitOrder`.
2. Modification includes using of `CQL`.
    ```js
    this.on('submitOrder', async (req) => {
        const { bookId, quantity } = req.data;
        const { Books } = cds.entities;
        const bookResponse = await SELECT.one(Books).where({ ID: bookId });
        if (!bookResponse) {
            req.reject(412, 'Book Id is invalid');
        }
        if (bookResponse.stock <= 0) {
            req.reject(412, 'Out of stock!');
        }
        if (quantity > bookResponse.stock) {
            req.reject(412, `Order exceed stock. Available stock is: ${bookResponse.stock}`);
        }
        return await UPDATE(Books, bookId).set({
            stock: bookResponse.stock - quantity
        });
    });
    ```

## Execute POST HTTP Request
### Steps
1. Open `bookshop-request.http`.
2. Search for request on `submitOrder` with POST operation.
3. Click `Send Request`.

## Response from HTTP Request
### Success Response
<kbd> ![Description](images/Day4-Exercise2-POST-Response-1.png)</kbd>

### Error Response
To achive this error, kindly send again a **POST Request**
<kbd> ![Description](images/Day4-Exercise2-POST-Response-2.png)</kbd>

## Database record updated
1. After executing `HTTP request`, the local database should be updated.<br>   
<kbd> ![Description](images/Day4-Exercise2-POST-Response-3.png) </kbd>