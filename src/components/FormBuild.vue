<template>
    <form class="form_build">
        <div class="form_build__wrapper">
            <div class="form_build__inputs">
                <Counts title="Количество комнат" />
                <FromTo title="Площадь, м" />
                <FromTo title="Стоимость, ₽" />
                <Selected title="Новостройка" :option_list="city" />
                <Selected title="Район" :option_list="area" />
                <InputBox title="Срок сдачи" />
            </div>
            <div class="form_build__btns">
                <Btn />
            </div>
        </div>
    </form>
</template>

<script>
import FromTo from '@/components/FromTo'
import Selected from '@/components/Selected'
import InputBox from '@/components/InputBox'
import Btn from '@/components/Btn'
import Counts from '@/components/Counts'
export default {
    name: 'FromBuild',
    components: {
        FromTo, 
        Selected,
        InputBox,
        Btn,
        Counts
    },
    data() {
        return {
        city: [
            {
                id: null,
                title: "Выберите город",
                select_value: ""
            },
            {
                id: 0,
                title: "Щелково",
                select_value: "Ch"
            },
            {
                id: 1,
                title: "Большие жеребцы",
                select_value: "BJ"
            },
            {
                id: 2,
                title: "Петушки",
                select_value: "P"
            },
        ],
        area: [
                {
                    id: null,
                    title: "Выберите район",
                    select_value: ""
                },
                {
                    id: 0,
                    title: "Беляева",
                    select_value: "bl"
                },
                {
                    id: 1,
                    title: "Перловская",
                    select_value: "pl"
                },
                {
                    id: 2,
                    title: "Арена",
                    select_value: "a"
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
.form_build {
    width: 100%;
    background-color: #fff;
    padding: 50px;
    &__wrapper{
        width: 70%;
        margin: 0 auto;
    }
    &__inputs {
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
    }
    &__btns{
        margin-top: 20px;
    }
}
</style>