<script>

import Discord from '@/assets/icons/discord.png'
import Facebook from '@/assets/icons/facebook.png'
import Dribbble from '@/assets/icons/dribbble.png'
import Instagram from '@/assets/icons/nstagram.png'
import Behance from '@/assets/icons/behance.png'

export default {
  data() {
    return {
      formData: {},
      defaultValue: '',
      imagePath: [
        {
          'path': Discord,
        },
        {
          'path': Facebook,
        },
        {
          'path': Dribbble,
        },
        {
          'path': Instagram,
        },
        {
          'path': Behance
        }
      ]
    }
  },
  methods: {
    submitEvent(event) {
      event.preventDefault()

      const data = { ...this.formData }

      const message = this.formData.message.replace(" ","%20")
      const whatsMessage = `https://wa.me//5541987560475?text=*Nome*:%20${this.formData.username}%20%0A*E-mail*%20${this.formData.email}%20%0A*Mensagem*%20${message}`
  
      
      let confirmeBox = confirm("Você será redirecionado ao whatsApp")
      confirmeBox == true ? window.open(whatsMessage, '_blank') : alert("Permissão negada, informações não enviadas :(")      
      
      document.getElementById('form').reset()
      console.log(JSON.stringify(data));

    },
    updateValue(event) {
      const inputName = event.target.name
      const upgradedValue = event.target.value

      this.formData[inputName] = upgradedValue
    }
  }
}

</script>

<template>
  <main id="container">
    <div class="text">
      <div class="textContent">
        <span>Lets work together</span>
        <p>This is a template Figma file, turned into code using Anima. Learn more at AnimaApp.com This is a template
          Figma
          file, turned into code using Anima. Learn more at AnimaApp.com</p>
        <div class="icons">
          <a v-for="x in imagePath">
            <img :src="x.path" alt="">
          </a>
        </div>
      </div>
    </div>
    <form class="form" id="form" @submit='submitEvent'>
      <input 
      class="inputClass"
      placeholder="Name" 
      type="text" 
      name="username" 
      @keyup="updateValue" 
      :value="defaultValue"
      required="true"
      >

      <input 
      class="inputClass"
      placeholder="Email" 
      type="text" 
      name="email" 
      @keyup="updateValue"
      required="true"
      >

      <textarea 
      class="inputClass"
      id="longInput" 
      placeholder="Type your message here" 
      name="message" 
      type="text" 
      rows="10"
      @keyup="updateValue"
      required="true"
      ></textarea>
      <button type="submit">submit</button>

    </form>
  </main>
</template>

<style scoped>
#container {
  margin-top: 100px;


  width: 100%;

  margin-bottom: 250px;

  display: flex;
  flex-direction: row;

}

.text {
  width: 50%;
}

.textContent {
  width: 60%;
}

span {
  font-weight: 600;
  font-size: 2rem;
}

p {
  font-weight: 400;
  font-size: 1.2rem;
  margin-top: 40px;
  margin-bottom: 40px;
}

.icons {
  text-decoration: none;
  list-style: none;

  display: flex;
  flex-direction: row;

  justify-content: flex-start;
  align-items: center;
}

.icons img {
  height: 40px;
  width: 40px;
  margin-left: 10px;
}

.form {
  width: 50%;
  display: flex;
  flex-direction: column;
}

.form input,
.form textarea {
  padding: 20px;
  margin-bottom: 20px;

  background-color: #F3F3F3;
  color: #2D2D2D;

  border: none;

  font-family: "Epilogue", sans-serif;
  font-weight: 600;
}

.form button {
  background-color: #2D2D2D;
  color: white;

  width: 235px;
  height: 80px;

  font-weight: 800;
  font-size: 1.2rem;

  transition: 1s ease-in-out;

  border: none;
}

.form button:hover {
  /*   background-color: #727272;
 */
  border-radius: 100px;
  box-shadow: 5px 5px 1px #F3AFA8;
}

@media (max-width: 600px) {
  #container {
    flex-direction: column;
    justify-content: center;
    text-align: center;
  }

  .textContent {
    width: 95vw;
    padding-bottom: 20px;
  }

  .form {
    width: 95vw;
    align-items: center;
  }

  .form input,
  .form textarea {
    width: 80vw;
  }

  .icons {
    justify-content: space-around;
  }

  .form button {
    width: 150px;
    height: 50px;

    border-radius: 10px;
  }

}
</style>
