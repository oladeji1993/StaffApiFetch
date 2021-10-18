
<template>
    <h1>Question 3. (Palindrome)</h1>
    <form>
        <div>
        <label>word to check</label>
        <input v-model="word" />
        </div>
    </form>
    <div>Is Palindrome:{{ isPalindrome ? "Yes" : "No" }}</div>
</template>

<script>
export default {
  name: "Palindrome",
  data() {
    return {
      word: "",
    };
  },
  computed: {
    isPalindrome() {
      const { word } = this;
      return word === word.split("").reverse().join("");
    },
  },
};
</script>

