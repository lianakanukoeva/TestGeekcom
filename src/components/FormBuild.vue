<template>
    <div class="form_build">
    <FromTo title="Площадь, м" />
    <FromTo title="Стоимость, ₽" />
    <Selected title="Новостройка" :option_list="city" />
    <Selected title="Район" :option_list="area" />
    <InputBox title="Срок сдачи" />
    <Btn />
    </div>
</template>

<script>
import FromTo from '@/components/FromTo'
import Selected from '@/components/Selected'
import InputBox from '@/components/InputBox'
import Btn from '@/components/Btn'
export default {
    name: 'FromBuild',
    components: {
        FromTo, 
        Selected,
        InputBox,
        Btn
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
.form_build{
    background-color: #fff;
}
</style>