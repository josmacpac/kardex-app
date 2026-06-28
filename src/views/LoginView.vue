<template>
  <!-- bg-bg-dark aplica tu fondo personalizado ultra oscuro -->
  <div class="min-h-screen flex items-center justify-center bg-bg-dark px-4">
    <!-- bg-card-dark y border-border-dark arman la tarjeta como la del monitor de stock -->
    <div class="max-w-md w-full space-y-8 bg-card-dark p-8 rounded-2xl shadow-2xl border border-border-dark">
      
      <!-- Encabezado inspirado en el diseño -->
      <div class="text-center">
        <!-- Badge verde esmeralda como el de "GESTIÓN DE ALMACÉN SIMPLICADA" -->
        <span class="inline-block px-3 py-1 text-xs font-semibold text-brand-emerald bg-brand-emerald-dim rounded-full uppercase tracking-wider mb-4">
          v1.0 Pre-despliegue
        </span>
        <h1 class="text-3xl font-extrabold text-white tracking-tight">
          KARDEX<span class="text-brand-emerald">.</span>
        </h1>
        <p class="mt-2 text-sm text-gray-400">Ingresa tus credenciales para acceder al sistema</p>
      </div>

      <!-- Formulario -->
      <form class="mt-8 space-y-6" @submit.prevent="manejarLogin">
        <div class="space-y-4">
          <!-- Correo -->
          <div>
            <label for="email" class="block text-sm font-medium text-gray-400">Correo Electrónico</label>
            <input 
              v-model="email"
              id="email" 
              type="email" 
              required 
              class="mt-1 block w-full px-3 py-2 bg-card-inner border border-border-dark rounded-lg text-white placeholder-gray-500 focus:outline-none focus:ring-2 focus:ring-brand-cyan focus:border-transparent"
              placeholder="usuario@y3n.store"
            />
          </div>

          <!-- Contraseña -->
          <div>
            <label for="password" class="block text-sm font-medium text-gray-400">Contraseña</label>
            <input 
              v-model="password"
              id="password" 
              type="password" 
              required 
              class="mt-1 block w-full px-3 py-2 bg-card-inner border border-border-dark rounded-lg text-white placeholder-gray-500 focus:outline-none focus:ring-2 focus:ring-brand-cyan focus:border-transparent"
              placeholder="••••••••"
            />
          </div>
        </div>

        <!-- Botón de Entrar usando el degradado azul-cian de la palabra "inventario" -->
        <div>
          <button 
            type="submit" 
            class="w-full flex justify-center py-2 px-4 rounded-lg text-sm font-semibold text-white bg-gradient-to-r from-brand-emerald to-brand-cyan hover:opacity-90 focus:outline-none focus:ring-2 focus:ring-brand-cyan transition-all shadow-lg"
          >
            Iniciar Sesión
          </button>
        </div>
      </form>

    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const email = ref('')
const password = ref('')

const manejarLogin = () => {
  alert(`Conectando... ${email.value}`)
}
</script>