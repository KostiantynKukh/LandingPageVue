<template>
  <div>
    <intro-contact />
    <feedback-form />
  </div>    
</template>

<script>
import IntroContact from '@/components/IntroContact'
import FeedbackForm from '@/components/FeedbackForm'

export default {
  name: 'Contact',
  components: {
    IntroContact,
    FeedbackForm
  }  
}
</script>