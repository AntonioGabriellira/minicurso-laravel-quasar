<template>
    <div class="q-ma-lg"> 
        <div class="text-h5"> 
            Listar currículo 
        </div>

        <div class="q-my-lg">
            <q-list bordered separator>
                <q-item clickable v-ripple v-for="curriculo in curriculos" :key="curriculo.id">
                    <q-item-section>
                        <q-item-label>
                            {{ curriculo.full_name }}
                        </q-item-label>
                        <q-item-label caption>
                            {{ curriculo.email }}
                        </q-item-label>
                    </q-item-section>
                </q-item>
            </q-list>
        </div>
    </div>
</template>

<script>
import {ref} from "vue";

export default{
    setup(){
        const curriculos = ref([
            { id: 1, 
                full_name: 'Antonio Gabriel sousa lira',
                first_name: 'A_gabriel', 
                last_name: 'lira',
                email:'ant@gmail.com',
                confirmado: 0,
            },
            { id: 2, 
                full_name: 'Romario marinho silva',
                first_name: 'Romario', 
                last_name: 'silva',
                email:'silva@gmail.com',
                confirmado: 0,
            },
            { id: 3, 
                full_name: 'Silvana de soares',
                first_name: 'Silvana', 
                last_name: 'soares',
                email:'soares@gmail.com',
                confirmado: 0,
            },
        ]);

        return {
            curriculos,
        };
    },
};
</script>

<style lang="css" scoped> </style>
