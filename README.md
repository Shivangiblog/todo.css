# todo.css
{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {

    background: linear-gradient(45deg, rgb(80, 25, 230) 45%,white 50%, rgb(130, 137, 240) 30%);
    align-items: center;
    display: flex;
    flex-direction: column;
    font-family: 'Work Sans', sans-serif;
    min-height: 100vh;
    padding-top: 3%;
}


.standard {
    background-image: linear-gradient(100deg, #8ab82f, #adbfe6);
    color: #fa12ad;
    transition: 0.3s linear;
    overflow: hidden;
}


#header, #form, #datetime {
    margin: 0 1rem;
    min-height: 10vh;
    min-block-size: 25%;
    width: 40%;
}
#datetime{
    font-size: x-large;
}

#header {
    align-items: center;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    font-size: 3rem;
    min-height: 25vh;
    width: 100%;
}

/* Theme buttons div */

.flexrow-container {
    align-items: center;
    align-self: center;
    display: flex;
    justify-content: space-around;
    margin-right: 2%;
}


/* Animation */
#title {

    white-space: pre;
    overflow: hidden;     
    letter-spacing: 0.20rem;
    margin-top: 50px;
    margin-bottom: 20px;
    max-width: 480px;
  }

  /* Animation */

#title {
    animation: animated-text 2s steps(11,end) 0.5s 1 normal both,
        animated-cursor 750ms steps(11,end) infinite;
  }

#title.darker-title {
    animation: animated-text 2s steps(11,end) 0.5s 1 normal both, darker-animated-cursor 750ms steps(11,end) infinite;
}

  /* text animation */


  @keyframes animated-text{
    from{width: 0%;}
    to{width: 480px;}
  }


form {
    display: flex;
    font-size: 1.7rem;
    justify-content: center;
    margin: 15px 0;
    padding: 0.8rem;
    width: 100%;
}

form input {
    padding: 10px;
    font-size: 17px;
    border: none;
    outline: none;
    /* border-radius: 18; */
    border-top-left-radius: 17px;
    border-bottom-left-radius: 17px;
    max-width: 450px;
    transition: background-color 200ms ease-in-out;
    width: 100%;
}



button {
    border: none;
    outline: none; 
    transition: box-shadow 200ms ease, background-color 200ms ease-in-out;
}

button:hover {
    cursor: pointer;
}

/* Button themes */
button.standard-button {
    background-color: rgb(247, 226, 223);
    color: rgb(0, 0, 0);
}

button.standard-button:hover {
    background-color: rgb(255, 255, 255);
    box-shadow: #fff8 0 0 10px;
}

form button {
    padding: 10px;
    font-size: 17px;
    border-top-right-radius: 15px;
    border-bottom-right-radius: 15px;
    min-width: 100px;
}

#myUnOrdList {
    color: #white;
    display: flex;
    justify-content: center;
    align-items: center;
    max-width: 1200px;
}

.todo-list {
    min-width: 25%;

    /* To remove the bullets of unordered list */
    list-style: none;
}

.todo {
    margin: 1rem;

    font-size: 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0.25em 0.5em;
    border-radius: 30px;
    transition: background-color 200ms ease-in-out;
}

/* Items themes */
.standard-todo {
    background-color: rgb(53, 177, 177);
}

.todo li{
    padding: 7px;

    font-size: 20px;
    flex: 1; /* To push the trash and the check button to the right */
    border-radius: 30px;

    /* wraps the links */
    overflow-wrap: anywhere;
}

.check-btn, .delete-btn {
    font-size: 19px;
    cursor: pointer;
    width: 2em;
    height: 2em;
    border-radius: 80%;
    margin: 0 5px;
}

.todo-item {
    padding: 0rem 0.5rem;
}

.fa-trash, .fa-check { 
    pointer-events: none;
}


.completed {
    transition: 0.2s;
    text-decoration: line-through;
    opacity: 0.5;
}

.fall {
    transition: 0.5s;
    transform: translateY(45rem) rotateZ(45deg);
    opacity: 0;
}

/* Responsive design */
@media only screen and (max-width: 1000px) {
    .flexrow-container {
        align-self: unset;
        margin-right: 0;
    }
}

@media only screen and (max-width: 800px) {
    #header {
        font-size: 2rem;
    }

    #title {
        animation: 
            animated-text 3s steps(16,end) 0.5s 1 normal both,
            animated-cursor 750ms steps(16,end) infinite;
        margin-bottom: 10px;
        margin-top: 30px;
        max-width: 330px;
    }
}

@media only screen and (max-width: 400px) {
    #header {
        font-size: 1.5rem;
    }

    #title {
        animation: 
            animated-text 3.5s steps(16,end) 0.5s 1 normal both,
            animated-cursor 750ms steps(16,end) infinite;
        max-width: 255px;
    }
}

@media only screen and (max-width: 400px) {
    form {
        align-items: center;
        flex-direction: column;
    }

    form input {
        border-radius: 17px;
    }

    form button {
        border-radius: 15px;
        margin-top: 15px;
        width: 50%;
    }
    form > button.light-button {
        box-shadow: 0 0 5px lightgray;
    }
}
