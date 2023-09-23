# Portfolio_Mahesh_Das

✅Created my own portfolio project using HTML, CSS and Javascript. Connected the contact form using Google Excel sheet.<br/>
Also, This portolio is live and hosted through gitHub.<br/>



✅Here is the code through which I connected my contact me form using excel:👇🏻<br/>

const scriptURL = 'Your google sheet link'<br/>
const form = document.forms['submit-to-google-sheet']<br/>
const msg = document.getElementById("msg")<br/>

form.addEventListener('submit', e => {<br/>
  e.preventDefault()<br/>
  fetch(scriptURL, { method: 'POST', body: new FormData(form)})<br/>
    .then(response => {<br/>
        msg.innerHTML = "Message Sent successfully"<br/>
        setTimeout(function(){<br/>
            msg.innerHTML = ""<br/>
        },5000)<br/>
        form.reset()<br/>
    })<br/>
    .catch(error => console.error('Error!', error.message))<br/>
})<br/>




