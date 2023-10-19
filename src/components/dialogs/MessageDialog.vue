<template>
    <v-dialog width="500" v-model="showMessageDialog" persistent>
        <template>
            <v-card title="Dialog">
                <v-card-text>
                    <br>
                   <strong> {{ message }} </strong>
                </v-card-text>

                <v-card-actions>
                    <v-spacer></v-spacer>

                    <v-btn text="OK" @click="$emit('closeMessageDialog')" class="warning alert-button">OK</v-btn>
                </v-card-actions>
            </v-card>
        </template>
    </v-dialog>
</template>

<script>
export default{
    name: 'MessageDialog',
    
    props:['message'],

    data(){
        return{
            showMessageDialog: true
        }
    }

}

</script>

<style scoped>
.alert-button{
    color: #FFF;
}

</style>