<template>
    <a-card class="youtube-card">
        <a-card-meta>
            <template #avatar>
                <a-avatar :src="avatarSrc" />
            </template>
            <template #title>
                <div style="display: flex; align-items: baseline; gap: 5px;">
                    <h2>Креативный канал Томо</h2>
                    <InfoCircleTwoTone />
                </div>
                <a-tag color="green">Аниме и комиксы</a-tag>
                <a-tag color="blue">Искусство и фото</a-tag>
            </template>
            <template #description>
                <a-popover placement="left">
                    <template #title>
                        <div><b>О блогере</b></div>
                    </template>
                    <template #content>
                        <div style="max-width: 300px;">Привет гости, на связи FOSTI. Канал "FOSTI" посвещён урокам или же
                            туториалам для начинающих ютуберов, по типу как сделать оформление канала, как сделать превью,
                            как поднять подписчиков и многое другое. Здесь ты научишься азам Photoshop'a, Cinema 4d и многим
                            другим. Подпишись и лето увеличивается на 1 месяц!</div>
                    </template>
                    <div class="youtube-card-description">
                        <div class="text">Привет гости, на связи FOSTI. Канал "FOSTI" посвещён урокам или же
                            туториалам для начинающих ютуберов, по типу как сделать оформление канала, как сделать превью,
                            как
                            поднять подписчиков и многое другое. Здесь ты научишься азам Photoshop'a, Cinema 4d и многим
                            другим.
                            Подпишись и лето увеличивается на 1 месяц!</div>
                    </div>
                </a-popover>

            </template>
        </a-card-meta>
        <div class="youtube-card-data">
            <div>ER</div>
            <div>Подписчики</div>
            <div>Просмотры</div>
            <div>Цена за обзор</div>
            <div>ER</div>
            <div style="display: flex; flex-direction: column; gap: 5px;">
                <a-button type="primary">Связаться</a-button>
                <a-button>Полный анализ</a-button>
                <a-button>Контакты</a-button>
            </div>
        </div>
    </a-card>
</template>
<script>
import { InfoCircleTwoTone } from "@ant-design/icons-vue";
export default {
    components: {
        InfoCircleTwoTone
    },
    props: {
        avatarSrc: String
    }
}
</script>
