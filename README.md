# GithubProfileInfo

### You can get info of any GitHub user by entering username

### View the site:

## Source Code

### HTML CODE:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Get Github Profile Info</title>
    <!-- CSS -->
    <link rel="stylesheet" href="./styles.css">
    <!-- fontawesome Link -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css" integrity="sha512-z3gLpd7yknf1YoNbCzqRKc4qyor8gaKU1qmn+CShxbuBusANI9QpRohGBreCFkKxLhei6S9CQXFEbbKuqLg0DA==" crossorigin="anonymous" referrerpolicy="no-referrer" />
</head>

<body>

    <!-- Get Github Profile Info by entering username of Github -->

    <main>

        <!-- heading -->
        <h1 class="heading">Get Github Profile Info</h1>

        <!-- form started -->
        <form>
            <!-- Enter your username -->
            <input id="input" type="text" placeholder="Enter your github username">
            <!-- submit button -->
            <button>Submit</button>
        </form>
        <!-- form ended -->

        <!-- profile card started -->
        <div class="loaders">
            <img src="./images/loader.gif" alt="">
        </div>
        <div class="profile-card">
               <p class="title">To display the information please enter the github username in the above field</p>
        </div>
        </div>
        <!-- profile card ended -->

        <!-- modal started -->
        <div class="modal"></div>
        <!-- modal ended -->
    </main>




    <!-- JavaScript -->
    <script src="./script.js"></script>
</body>

</html>

```

### CSS CODE:

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, Helvetica, sans-serif;
}

/* body and html */
body,
html {
  width: 100%;
  height: 100vh;
  font-size: 10px;
}
/* common CSS */
img {
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -o-user-select: none;
  user-select: none;
}

/* main Started */

main {
  width: 100%;
  height: 100%;
  padding: 2em 3em;
  background-color: white;
}

/* heading */
.heading {
  font-size: 3em;
  color: rgb(17, 57, 72);
  font-weight: 800;
  text-align: center;
  margin-top: 1em;
}

/* form started */

form {
  display: flex;
  flex-direction: column;
  width: 100%;
  max-width: 40em;
  margin: 1em auto;
  padding: 1.5em;
}

form input {
  padding: 1em;
  border: 0;
  outline: none;
  border-radius: 5px;
  font-size: 1.5em;
  font-weight: bold;
  color: rgb(6, 62, 85);
  box-shadow: inset 4px 4px 2px rgba(0, 0, 0, 0.3), inset -3px -3px 15px rgb(237, 237, 237);
}
form button {
  margin: 1em auto;
  padding: 10px 25px;
  border-radius: 3px;
  font-size: 1.8em;
  cursor: pointer;
  border: 0;
  background-color: rgb(14, 62, 79);
  color: white;
  transition: all ease 0.5s;
}
form button:active {
  transform: scale(0.8);
}

/* form ended */

/* loader */
.loaders {
  text-align: center;
  margin-bottom: 20px;
  display: none;
}
.loaders img {
  width: 40px;
}

/* profile card started */

.profile-card {
  max-width: 60em;
  margin: auto;
  background-color: rgb(251, 251, 252);
  height: fit-content;
  padding: 20px;
  border-radius: 5px;
  box-shadow: 1px 1px 10px rgba(0, 0, 0, 0.3);
  position: relative;
}
.profile-card .title {
  text-align: center;
}
.profile-card p {
  font-size: 1.5em;
  font-weight: bold;
  color: rgb(20, 53, 66);
  margin: 8px 0;
}
.profile-card p span {
  color: rgb(30, 120, 155);
}

.profile-card p a {
  color: rgb(18, 148, 31);
}

.profile-card p a:hover {
  color: rgb(20, 53, 66);
}

.profile-card img {
  float: right;
  width: 120px;
  height: 120px;
  border-radius: 50%;
  box-shadow: 2px 2px 15px rgba(0, 0, 0, 0.5);
  cursor: pointer;
  transition: all ease 0.3s;
}
.profile-card img:hover {
  transform: scale(0.9);
}
.profile-card i {
  font-size: 25px;
  color: rgb(243, 102, 87);
  cursor: pointer;
  position: absolute;
  top: -10px;
  right: -10px;
  padding: 4px 8px;
  border-radius: 50%;
  background-color: rgb(226, 226, 226);
  box-shadow: 1px 1px 4px rgba(0, 0, 0, 0.5);
}
.profile-card i:hover {
  box-shadow: 1px 1px 8px rgba(0, 0, 0, 0.8);
}
/* profile card ended */

/* modal started */

.modal {
  width: 100%;
  height: 100vh;
  background-color: rgba(0, 0, 0, 0.5);
  position: absolute;
  top: 0;
  left: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: -1;
}
.modal .pop-up {
  position: relative;
}
.modal img {
  border-radius: 50%;
}
.modal i {
  font-size: 4em;
  position: absolute;
  top: 0;
  cursor: pointer;
  transition: all ease 0.5s;
  padding: 5px 10px;
  border-radius: 50%;
}
.modal i:hover {
  transform: rotate(180deg);
  background-color: rgb(239, 79, 79);
}

/* modal ended */

/* main ended */

@media screen and (max-width: 500px) {
  body,
  html {
    font-size: 9px;
  }
  .profile-card {
    padding: 15px;
  }
  .modal img {
    width: 250px;
  }
  .modal i:hover {
    transform: none;
    background-color: transparent;
  }
  .profile-card img:hover {
    transform: none;
  }
}
```

### JAVASCRIPT CODE:

```javascript
// Logic

// select form field and get the value of input
const form = document.querySelector("form");
const input = document.querySelector("#input");
let valueOfUser;
form.addEventListener("submit", (e) => {
  e.preventDefault();
  valueOfUser = String(input.value);
  if (valueOfUser === "") {
    return alert("Please enter the github username");
  }
  fetchData();
});

// fetch data
let userData;
let createdAtdate;
let updatedAtdate;
const fetchData = async () => {
  try {
    const response = await fetch(`https://api.github.com/users/${valueOfUser}`);
    userData = await response.json();
    createdAtdate = new Date(userData.created_at).toLocaleDateString();
    updatedAtdate = new Date(userData.updated_at).toLocaleDateString();
  } catch (error) {
    console.log("E: " + error);
  }
  input.value = "";
  showLoader();
};

// showLoader
const showLoader = () => {
  const loader = document.querySelector(".loaders");
  loader.style.display = "block";
  setTimeout(() => {
    loader.style.display = "none";
    showData();
  }, 500);
};

// showData
const card = document.querySelector(".profile-card");
const showData = () => {
  card.innerHTML = `
        <img class="profileImg" src="${userData.avatar_url}" alt="">
        <p> <span>Name:</span> ${
          userData.message === "Not Found" ? "Not found" : userData.name
        }</p>    
        <p> <span>Username:</span> ${
          userData.message === "Not Found" ? "Not found" : userData.login
        }</p>    
        <p> <span>Followers:</span> ${
          userData.message === "Not Found" ? "Not found" : userData.followers
        }</p>    
        <p> <span>Following:</span> ${
          userData.message === "Not Found" ? "Not found" : userData.following
        }</p>    
        <p> <span>Public Repository:</span> ${
          userData.message === "Not Found" ? "Not found" : userData.public_repos
        }</p>    
        <p> <span>Created at:</span> ${
          userData.message === "Not Found" ? "Not found" : createdAtdate
        }</p>    
        <p> <span>Updated at:</span> ${
          userData.message === "Not Found" ? "Not found" : updatedAtdate
        }</p>    
        <p> <span>Bio:</span> ${
          userData.message === "Not Found" ? "Not found" : userData.bio
        }</p>    
        <p> <span>Location:</span> ${
          userData.message === "Not Found" ? "Not found" : userData.location
        }</p>    
        <p> <span>Twitter:</span> <a target='_blank' href="https://twitter.com/${
          userData.twitter_username
        }">${userData.twitter_username}</a></p>    
        <p> <span>Blog:</span> <a target='_blank' href="${
          userData.message === "Not Found" ? "Not found" : userData.blog
        }">${userData.blog}</a></p>    
        <p> <span>Github Profile:</span> <a target='_blank' href="${
          userData.html_url
        }">${userData.html_url}</a></p>
        <i class="fa-solid fa-xmark closeCard"></i> 
        `;
  showModal();
};

// showModal
const showModal = () => {
  // Logic to show modal when user clicks on profile image
  // card Img
  const profileImg = document.querySelector(".profileImg");
  // modal
  let modal = document.querySelector(".modal");

  // modal innerHTML
  modal.innerHTML = `
        <div class="pop-up">
        <img class="modalImg" src="${userData.avatar_url}" alt="">
        <i class="fa-solid fa-xmark closeModal" style="color: #ffffff;"></i>
        </div>
        `;

  // eventListener to show modal
  profileImg.addEventListener("click", () => {
    modal.style.zIndex = "1";
  });

  // cross button for modal
  const crossIcon = document.querySelector(".closeModal");
  // eventListener to close modal
  crossIcon.addEventListener("click", () => {
    modal.style.zIndex = "-1";
  });

  // cross button for card
  const crossBtnForCard = document.querySelector(".closeCard");
  // eventListener to close modal
  crossBtnForCard.addEventListener("click", () => {
    card.innerHTML = `
           <p class="title">To display the information please enter the github username in the above field</p>
           `;
  });
};
```

### Techonologies Used

<li>HTML</li>
<li>CSS</li>
<li>JavaScript</li>
<li>GitHub API</li>