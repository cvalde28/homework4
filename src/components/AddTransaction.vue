<script setup>
    import {ref, defineEmits} from 'vue'
    const text = ref('')
    const amount = ref('')

    const emit = defineEmits([
        'transactionSubmitted'
    ])

    const onSubmit = () =>{
        const transactionData = {
            text: text.value,
            amount: paraseFloat(amount.value),
        }
        
        emit('transactionSubmitted', transactionData)
        
        text.value = ''
        amount.value = ''
    }



</script>

<template>

</template>