# Presentation-7

## API

> «Application Programming Interface»
>
>![](https://camo.githubusercontent.com/6eb616cc5401babd7ddcee71a9dc934a9914b3902b4acc66d915503fb9faef6c/68747470733a2f2f686f742d68617463682e72752f3830302f3630302f68747470732f777777322e746865626967626f782e69642f77702d636f6e74656e742f75706c6f6164732f323031392f30382f6f766572766965772e706e67)

### API VS REST API

> API is a general term that means "application programming interface".
>
>Rest API это конкретный API, под названием REST, описывающий протокол взаимодействия с веб сервисом.

## REST API

>![](https://camo.githubusercontent.com/beabb3f73874d32a60e828074819f784cd5a2cb1f90602b07dd5b4afee9e0823/68747470733a2f2f732e376c6561726e2e636f6d2f75706c6f6164732f323032302f30322f726573745f6170692e6a7067)

#### Fetch()

>The Fetch API provides a JavaScript interface for working with HTTP requests and responses. It also provides a global fetch()en US) method that makes it easy and logical to get resources over the asynchronous network

###### GET

const getUsers = async ( ) =>{
try{
const response = await fetch("");
const
data = await response.json
console.log(data);
}
catch(error){
console.log(error)
}
}

###### POST

const postUser = async (user) =>{
    try {
        const response = await fetch("",
        {
            method: "POST",
            headers: {
                accept: "application/json",
                "Content-Type": "application/json",
                },
                body: JSON.stringify(user),
        });
    } catch (error) {
        console.log(error);
    }
}

###### PUT

const putUser = async (id,edituser) =>{
    try {
        const response = await fetch("",
        {
            method: "PUT",
            headers: {
                accept: "application/json",
                "Content-Type": "application/json",
                },
                body: JSON.stringify(edituser),
        });
    } catch (error) {
        console.log(error);
    }
}

###### DELETE

const deleteUser = async (id) =>{
    try {
        const response = await fetch("",
        {
            method: "DELETE",
        });
    } catch (error) {
        console.log(error);
    }
}

### axios

>Axios is a simple promise based HTTP client for the browser and node.js. Axios provides a simple to use library in a small package with a very extensible interface.

### Using unpkg CDN:

> <script src="https://unpkg.com/axios/dist/axios.min.js"></script>

###### GET

const getUsers = async ( ) =>{
    try{
        const {data}= await axios.get('')
    } catch(error){
        console.log(error)
    }
}

###### POST

const postUser = async (user) =>{
    try {
        const {data}= await axios.post('',user)
    } catch (error) {
        console.log(error);
    }
}

###### PUT

const putUser = async (id,edituser) =>{
    try {
        const {data}= await axios.put(`url/${id}`,user)
    } catch (error) {
        console.log(error);
    }
}

###### DELETE

const deleteUser = async (id) =>{
    try {
        const {data}= await axios.delete(`url/${id}`)
    } catch (error) {
        console.log(error);
    }
}