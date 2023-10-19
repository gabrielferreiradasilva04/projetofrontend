<template>
    <v-row justify="center">
        <v-dialog v-model="dialog" persistent width="30%">
            <v-card>
                <v-card-title>
                    <span class="text-h5 title">Validação de E-mail</span>
                    <small>Caso não tenha recebido, verifique seu endereço de e-mail</small>
                </v-card-title>
                <v-card-text>
                    <v-container>
                        <v-row>
                            <v-col cols="12" sm="6" md="10">
                                <v-text-field label="Código" required></v-text-field>
                            </v-col>

                        </v-row>
                    </v-container>
                </v-card-text>
                <v-card-actions>
                    <v-spacer></v-spacer>
                    <!-- para criar funções durante o evento de clik podemos usar o $emit que manda uma mensagem para 
                    o componente pai indicando que ele deve executar o nétodo closeDialog -->
                    <v-btn color="yellow-darken-3" variant="text" @click="$emit('closeDialog')">
                        Finalizar
                    </v-btn>
                </v-card-actions>
            </v-card>
        </v-dialog>
    </v-row>
</template>

<script>
export default {
    data: () => ({
        dialog: true,
    }),
}
</script>
<style scoped>
.title {
    color: #F9A825;
    font-weight: bold;
}
</style>