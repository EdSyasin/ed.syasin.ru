<template>
    <div class="kek">
        <button @click="age++">{{test}}</button>
        <div>lol</div>
    </div>
</template>

<script lang="ts">
import { Vue, Component } from 'vue-property-decorator'

@Component({})
export default class ExampleComponent extends Vue{
    name: string = 'Eduard'
    age: number = 18

    get test(): number{
        return this.age + this.age;
    }

    mounted(): void {
        console.log("Component mounted")
    }
}
</script>

<style lang="scss">
$kek: #96a3de;

.kek{
    background-color: $kek;
    text-align: center;
}

</style>