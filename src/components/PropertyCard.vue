<template>
    <div>
        <div class="relative pb-5/6">
        <img class="absolute inset-0 h-full rounded-lg shadow-md object-cover" :src="property.imgUrl" alt="home1">
        </div>
        <div class="relative px-4 -mt-16">
        <div class="bg-white rounded-lg px-4 py-4 shadow-lg">
            <div class="flex">
            <span class="bg-teal-200 text-teal-800 font-medium uppercase tracking-wide text-xs rounded-full px-2 py-1 leading-none inline-block">PLUS</span>
            <div class="ml-2 text-xs text-gray-600 font-semibold uppercase tracking-wide">
                {{property.beds}} {{property.beds === 1 ? 'cama' : 'camas'}} &bull; {{property.baths}} {{property.baths === 1 ? 'baño' : 'baños'}}
            </div>
            </div>
            <h4 class="mt-1 text-gray-900 font-semibold text-lg">{{property.title}}</h4>
            <div class="mt-1">
            <span class="text-gray-900">{{formatedPrice}}</span><span class="mt-1 text-sm text-gray-600">/día</span>
            </div>
            <div class="text-sm text-gray-600 flex items-center mt-2">
            <svg v-for="i in 5" :key="i" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 56 53" class="h-4 w-4 fill-current" :class="property.rating > i ? 'text-teal-500' : 'text-gray-400'">
                <path d="M48.856 22.73c.983-.958 1.33-2.364.906-3.671-.425-1.307-1.532-2.24-2.892-2.438l-12.092-1.757c-.515-.075-.96-.398-1.19-.865L28.182 3.043c-.607-1.231-1.839-1.996-3.212-1.996-1.372 0-2.604.765-3.211 1.996L16.352 14c-.23.467-.676.79-1.191.865L3.069 16.622C1.71 16.819.602 17.753.177 19.06c-.424 1.307-.077 2.713.906 3.671l8.749 8.528c.373.364.544.888.456 1.4L8.224 44.701c-.183 1.06.095 2.091.781 2.904 1.066 1.267 2.927 1.653 4.415.871l10.814-5.686c.452-.237 1.021-.235 1.472 0l10.815 5.686c.526.277 1.087.417 1.666.417 1.057 0 2.059-.47 2.748-1.288.687-.813.964-1.846.781-2.904l-2.065-12.042c-.088-.513.083-1.036.456-1.4l8.749-8.529z"/>
            </svg>
            <span class="ml-2">{{property.reviewCount}} valoraciones</span>
            </div>
        </div>
        </div>
    </div>
</template>

<script>
export default {
    props: ['property'],
    computed: {
        formatedPrice() {
            const formatter = new Intl.NumberFormat('es-ES', {
                style: 'currency',
                currency: 'EUR'
            });

            return formatter.format(this.property.price);
        }
    }
}
</script>