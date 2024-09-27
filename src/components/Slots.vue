<template>
    <div class="componente">
        <h1>Componente com slots</h1>
        <button>
            <slot name="icone"></slot>
            <slot name="texto">
                Botão
            </slot>
        </button>
    </div>
</template>