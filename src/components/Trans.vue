<template>
    <div>
      <label>
        十进制:
        <input type="text" v-model="decimal" />
      </label>
      <label>
        原码:
        <input type="text" v-model="original" />
      </label>
      <label>
        反码:
        <input type="text" v-model="complement" />
      </label>
      <label>
        补码:
        <input type="text" v-model="twosComplement" />
      </label>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        decimal: '',
        original: '',
        complement: '',
        twosComplement: '',
      };
    },
    computed: {
      decimalComputed: {
        get() {
          return this.decimal;
        },
        set(value) {
          this.decimal = value;
          this.original = this.getOriginal(value);
          this.complement = this.getComplement(this.original);
          this.twosComplement = this.getTwosComplement(this.complement);
        },
      },
      originalComputed: {
        get() {
          return this.original;
        },
        set(value) {
          this.original = value;
          this.decimal = this.getDecimal(value);
          this.complement = this.getComplement(value);
          this.twosComplement = this.getTwosComplement(this.complement);
        },
      },
      complementComputed: {
        get() {
          return this.complement;
        },
        set(value) {
          this.complement = value;
          this.original = this.getOriginalFromComplement(value);
          this.decimal = this.getDecimal(this.original);
          this.twosComplement = this.getTwosComplement(value);
        },
      },
      twosComplementComputed: {
        get() {
          return this.twosComplement;
        },
        set(value) {
          this.twosComplement = value;
          this.complement = this.getComplementFromTwosComplement(value);
          this.original = this.getOriginalFromComplement(this.complement);
          this.decimal = this.getDecimal(this.original);
        },
      },
    },
    methods: {
      getOriginal(decimal) {
        const isNegative = decimal < 0;
        let binary = Math.abs(decimal).toString(2);
        return isNegative ? '1' + binary.slice(1).padStart(7, '0') : binary.padStart(8, '0');
      },
      getComplement(original) {
        return original.replace(/1/g, 'x').replace(/0/g, '1').replace(/x/g, '0');
      },
      getTwosComplement(complement) {
        return (parseInt(complement, 2) + 1).toString(2).padStart(8, '0');
      },
      getDecimal(original) {
        const isNegative = parseInt(original.charAt(0), 2);
        let decimal = parseInt(original.slice(1), 2);
        return isNegative ? -decimal : decimal;
      },
      getOriginalFromComplement(complement) {
        return complement.replace(/1/g, 'x').replace(/0/g, '1').replace(/x/g, '0');
      },
      getComplementFromTwosComplement(twosComplement) {
        return (parseInt(twosComplement, 2) - 1).toString(2).padStart(8, '0');
      },
    },
  };
  </script>