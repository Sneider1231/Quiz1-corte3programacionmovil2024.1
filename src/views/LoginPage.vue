<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title>REGISTROS</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Login</ion-title>
        </ion-toolbar>
      </ion-header>
      <div id="login-container">
        <!-- Componente de imagen -->
        <ImagenComponent id="miImagen" imageUrl="public\escudo fac simbolos (1).jpg" altText="imagen" />

        <div id="description">
          <p>Bienvenido a la fuerza aerea.</p>
          <p>Así se va a las Estrellas.</p>
        </div>
      
        <div id="login-form">
          <InputComponent id="user" name="Nombre" label="Nombre: " style="color: black;" />
          <InputComponent type="number" id="tel" name="Celular" label="Celular: " style="color: black;" />
          <InputComponent type="email" id="email" name="correo" label="Email: " style="color: black;" />
          <InputComponent type="date" id="date" name="Fecha_de_Nacimiento" style="color: black;" />

          <br>
          <ButtonComponent id="login" value="Consultar" fill="outline" color="black" />
          <ButtonComponent id="save" value="Agregar" fill="outline" color="primary"/>
          <ButtonComponent id="update" value="Modificar" fill="outline" color="warning"/>
          <ButtonComponent id="delete" value="Eliminar" fill="outline" color="danger"/>
        </div>
        
        <ion-button id="present-alert" class="custom-button">Registrar</ion-button>
        <ion-alert
          trigger="present-alert"
          sub-header="Base De datos Ingresado"
          message="Hemos ingresado tus datos, te vamos a poner en contacto."
          :buttons="alertButtons"
        ></ion-alert>
      </div>
    </ion-content>
  </ion-page>
</template>

<script setup lang="ts">
import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar,IonAlert, IonButton } from '@ionic/vue';
import ButtonComponent from '@/components/ButtonComponent.vue';
import InputComponent from '@/components/InputComponent.vue';
import ImagenComponent from '@/components/ImagenComponent.vue';
const alertButtons = ['Action'];
</script>

<style scoped>
#login-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100%;
  /* Agrega la imagen de fondo */
  background-image: url('public/AVIONES-FUERZA-AEREA.jpg');
  /* Ajusta el tamaño y la posición de la imagen */
  background-size: cover;
  background-position: center;
}

#cart-image {
  margin-bottom: 20px;
  width: 100px;
}

#description {
  margin-bottom: 20px;
  text-align: center;
}

#description p {
  margin: 0;
  padding: 10px; 
}

#login-form {
  max-width: 300px;
  width: 100%;
}

.custom-button {
  margin-top: 20px; /* Ajusta la distancia desde arriba */
  width: 200px; /* Ajusta el ancho del botón */
}
</style>
