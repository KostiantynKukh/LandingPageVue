<template>
  <div class="wrap feedback-form__wrapper">
    <form @submit.prevent="submit" class="feedback-form">

      <h2 class="section-title feedback-form__section-title">Contact Us</h2>

    <!-- FIRSTNAME START-->
      <div class="form-group" :class="{ 'form-group--error': $v.form.firstName.$invalid && form.submitStatus === 'ERROR' }">
          <label class="form__label">First name</label>
          <input class="form__input" placeholder="First name" type="text" v-model.trim="$v.form.firstName.$model"/>
          
        <!-- SHOW ERROR BLOCK START -->
          <div class="error" v-if="!$v.form.firstName.required && form.submitStatus === 'ERROR'">First name is required!</div>
          <div class="error" v-if="!$v.form.firstName.alpha && form.submitStatus === 'ERROR'">First name must contains only alphabet characters!</div>
          <div class="error" v-if="!$v.form.firstName.minLength && form.submitStatus === 'ERROR'">First name must have at least {{$v.form.firstName.$params.minLength.min}} letters!</div>
          <div class="error" v-if="!$v.form.firstName.maxLength && form.submitStatus === 'ERROR'">First name must have maximum {{$v.form.firstName.$params.maxLength.min}} letters!</div>
        <!-- SHOW ERROR BLOCK END --> 
      </div>        
    <!-- FIRSTNAME END-->

    <!-- LASTNAME START-->
      <div class="form-group" :class="{ 'form-group--error': $v.form.lastName.$invalid && form.submitStatus === 'ERROR' }">
          <label class="form__label">Last name</label>
          <input type="text" class="form__input" placeholder="Last name" v-model.trim="$v.form.lastName.$model"/>

        <!-- SHOW ERROR BLOCK START -->
          <div class="error" v-if="!$v.form.lastName.required && form.submitStatus === 'ERROR'">Last name is required!</div>
          <div class="error" v-if="!$v.form.lastName.alpha && form.submitStatus === 'ERROR'">Last name must contains only alphabet characters!</div>
          <div class="error" v-if="!$v.form.lastName.minLength && form.submitStatus === 'ERROR'">Last name must have at least {{$v.form.lastName.$params.minLength.min}} letters!</div>
          <div class="error" v-if="!$v.form.lastName.maxLength && form.submitStatus === 'ERROR'">Last name must have maximum {{$v.form.lastName.$params.maxLength.min}} letters!</div>
        <!-- SHOW ERROR BLOCK END --> 
      </div>        
    <!-- LASTNAME END-->

    <!-- PHONE START-->
      <div class="form-group" :class="{ 'form-group--error': $v.form.phone.$invalid && form.submitStatus === 'ERROR' }">
          <label class="form__label">Phone number</label>
          <div class="form-select__wrapper">
            <select name="country" @change="chooseCountry" v-model="selectedCountry" class="form-select" >
              <option v-for="(country, index) in countries" :key="index" class="form-select__option" :class="country.value" :value="country.value"><span v-if="selectedCountry !== country.value">{{country.name}}</span> {{ country.code }}</option>              
            </select>
            <input type="text" class="form__input" placeholder="123456789" v-model.trim="$v.form.phone.$model"/>
          </div>
          
        <!-- SHOW ERROR BLOCK START -->
          <!-- <div class="error" v-if="!$v.form.phone.required && form.submitStatus === 'ERROR'">First name is required!</div> -->
          <div class="error" v-if="!$v.form.phone.numeric && form.submitStatus === 'ERROR'">Phone number must contains only numeric characters!</div>
          <div class="error" v-if="!$v.form.phone.minLength && form.submitStatus === 'ERROR'">First name must have at least {{$v.form.phone.$params.minLength.min}} letters!</div>
          <div class="error" v-if="!$v.form.phone.maxLength && form.submitStatus === 'ERROR'">First name must have maximum {{$v.form.phone.$params.maxLength.min}} letters!</div>
        <!-- SHOW ERROR BLOCK END --> 
      </div>        
    <!-- PHONE END-->

    <!-- EMAIL START-->
      <div class="form-group" :class="{ 'form-group--error': $v.form.email.$invalid && form.submitStatus === 'ERROR' }">
          <label class="form__label">Email</label>
          <input type="text" class="form__input" placeholder="example@email.com" v-model.trim="$v.form.email.$model"/>
        <!-- SHOW ERROR BLOCK START -->

          <div class="error" v-if="!$v.form.email.required && form.submitStatus === 'ERROR'">Email is required!</div>
          <div class="error" v-if="!$v.form.email.email && form.submitStatus === 'ERROR'">Email is invalid!</div>
          <div class="error" v-if="!$v.form.email.minLength && form.submitStatus === 'ERROR'">Email must have at least {{$v.form.email.$params.minLength.min}} letters!</div>
          <div class="error" v-if="!$v.form.email.maxLength && form.submitStatus === 'ERROR'">Email must have maximum {{$v.form.email.$params.maxLength.min}} letters!</div>
        <!-- SHOW ERROR BLOCK END --> 
      </div>        
    <!-- EMAIL END-->

    <!--MESSAGE START-->
      <div class="form-group" :class="{ 'form-group--error': $v.form.message.$invalid && form.submitStatus === 'ERROR' }">
          <label class="form__label">Message</label>
          <textarea type="text" class="form__input form-textarea" placeholder="What would you like to discuss?" v-model.trim="$v.form.message.$model"></textarea>
        
        <!-- SHOW ERROR BLOCK START -->
          <div class="error" v-if="!$v.form.message.required && form.submitStatus === 'ERROR'">Message is required!</div>          
          <div class="error" v-if="!$v.form.message.minLength && form.submitStatus === 'ERROR'">Message must have at least {{$v.form.message.$params.minLength.min}} letters!</div>
          <div class="error" v-if="!$v.form.message.maxLength && form.submitStatus === 'ERROR'">Message must have maximum {{$v.form.message.$params.maxLength.min}} letters!</div>
        <!-- SHOW ERROR BLOCK END --> 
 
      </div>        
    <!-- MESSAGE END-->

    <!-- SUBMIT BUTTON START -->
      <w-button class="feedback-form__submit-button" color="dark" size="lg" type="submit" :disabled="form.submitStatus === 'PENDING'">Send</w-button>        
      <p class="submit-status" v-if="form.submitStatus === 'OK'">Thanks for your submission!</p>
      <p class="submit-status" v-if="form.submitStatus === 'ERROR'">Please fill the form correctly.</p>
      <p class="submit-status" v-if="form.submitStatus === 'PENDING'">Sending...</p>
    <!-- SUBMIT BUTTON END -->
    </form>
  </div>
</template>

<script>
import { required, minLength, maxLength, alpha, numeric, email } from 'vuelidate/lib/validators'
import WButton from '@/widgets/WButton'

export default {
  name: 'FeedbackForm',
  components: {
    WButton
  },
  data() {
    return {
      form: {
        firstName: '',
        lastName: '',
        phone: '',
        email: '',
        message: '',
        submitStatus: null        
      },
      selectedCountry: null,
      countries: [
          {
            name: 'Ukraine',
            value: 'ua',
            code: '+380'
          },
          {
            name: 'United Kingdom',
            value: 'gb',
            code: '+44'
          },
          {
            name: 'United Arab Emirates',
            value: 'ae',
            code: '+971'
          }  
        ]      
    }
  },   
  validations: {
    form: {
      firstName: {
        required,
        alpha,
        minLength: minLength(3),
        maxLength: maxLength(40)
      },
      lastName: {
        required,
        alpha,
        minLength: minLength(3),
        maxLength: maxLength(40)
      },
      phone: {        
        numeric,
        minLength: minLength(9),
        maxLength: maxLength(9),
        
      },
      email: {
        required,
        email,        
        minLength: minLength(5),
        maxLength: maxLength(40)
      },
      message: {
        required,
        minLength: minLength(30),
        maxLength: maxLength(1000)
      }
    }
  },
  methods: {
    chooseCountry() {
      console.log(this.selectedCountry);
    },
    submit() {
      this.$v.form.$touch()
      if (this.$v.form.$invalid) {
        this.form.submitStatus = 'ERROR'
      } else {
        // do your submit logic here
        this.form.submitStatus = 'PENDING'
        setTimeout(() => {
          this.form.submitStatus = 'OK'
        }, 500)
      }
    }
  }
}
</script>

<style lang="scss" scoped>

.feedback-form__wrapper {
  display: flex;
  justify-content: center;
  padding: 20px 0;
}

.feedback-form {
  width: 100%;
  padding: 0 15px;
  max-width: 340px;  
}

.feedback-form__section-title {
  text-align: center;
  margin-bottom: 20px;
}

.form-group {
  min-height: 71px;
}

.form__label {
  display: block; 
  font-size: 1.2rem;
  color: #111B47;
  margin-bottom: 2px;
  padding-left: 10px;   
}

.form__input, .form-select {
    box-sizing: border-box;
    display: block;
    width: 100%;
    height: 40px;    
    margin: 0;
    padding: 5px 10px;
    background-color: #fff;
    border: 1px solid #adb2c2;
    border-radius: 3px;
    font-size: 16px;
    color: #2b3d52;
    line-height: 1.4rem;
    outline: none;
    margin-bottom: 2px;

    &:focus {
      border: 2px solid #5a6485;
    }
}

.form-select__wrapper {
  display: grid;
  grid-template-columns: 1fr 2fr;
  
}

.form-group--error {
  .form__label {
    color: red;
  }
  .form__input {
    border: 2px solid red;
  }  
}

.error {
  color: red;
  padding-left: 10px;
  font-size: 1.2rem;
}

.feedback-form__submit-button {
  margin: 10px 0 10px 50%;
  transform: translateX(-50%);
}

.form-textarea {
  resize: none; 
  height: 100px; 
  padding: 10px;
  max-width: 100%;
}

.submit-status {
  color: #111B47;
  font-size: 1.6rem;
  text-align: center;
}

</style>