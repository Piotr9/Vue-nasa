<template>
      <input
        id="search"
        name="search"
        :value="value"
        @input="handleChange"
      />
</template>

<script>
export default {
  name: 'SearchInput',
  props: {
    value: {
      type: String,
      required: true,
      default: '',
    },
  },
  methods: {
    handleChange(e) {
      this.$emit('input', e.target.value);
    },
  },
};
</script>

<style lang="scss" scoped>
    input {
        margin-top: 50px;
        display: flex;
        flex-direction: column;
        width: 300px;
        color: white;
        text-align: center;
        font-size: 18px;
        height: 30px;
        border: 0;
        background: none;
        border-bottom: 1px solid white;
        transition: box-shadow .5s;

        @media (min-width: 1024px) {
            font-weight: 400;
        }
    }

    input:focus {
        outline: none;
        box-shadow: 0 10px 20px -8px rgba($color: white, $alpha: .5);
        background: none;
    }
</style>
