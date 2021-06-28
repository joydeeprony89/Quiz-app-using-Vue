<template>
  <div class="result">
      <div class="title">{{ getResult.title }}</div>
      <div class="desc">{{ getResult.desc }}</div>
    </div>
</template>

<script>
export default {
    props:["results", "correctAnswers"],
    computed: {
        getResult() {
            var answer = [];
             if(this.correctAnswers == 3) 
                answer = this.results[1];
             else 
                answer = this.results[0];

            return answer;
        }
    }
}
</script>