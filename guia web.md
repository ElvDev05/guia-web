##Crear entidad en el directorio model de nuestro bounded context

- Creamos archivo "entidad.entity"



## Construccion de API Service
- Importar Axios:
	import axios from 'axios';

- Creamos constante http:
	const http = axios.create({
   	 baseURL: '*LA URL BASE DEL API*'
	});

- Creamos la clase de nuestro services

- Creamos metodo para retornar http:

	getCountries(){
       return http.get('name/peru');
   }
//ejemplos

 getSources() {
        return http.get(`top-headlines/sources?apiKey=${this.apiKey}`);
    }

    getArticlesForSource(sourceId) {
        return http.get(`top-headlines?sources=${sourceId}&apiKey=${this.apiKey}`);
	
## En el main.js

- Realizar los import de PrimeVue para Material Design

- Realziar el PrimeVue Setup ( Ejemplo):

	app.use(PrimeVue, {ripple:true})
	.component('pv-card', Card)
	.component('pv-toolbar', Toolbar)
	.component('pv-avatar', Avatar);

## En los componentes de bounded context
### En el componente que almacenara la entidad

- Importar la entidad en el componente

- Agregar los properties en el scrip:

	<script>
	export default {
  	name: "country-card"

	}


### Para la creacion del componente 

- Utilizar plantilla de PRIME VUE y reemplazar , ejemplo:pv-card 

- Si el problema pide iterar , podemos usar v-for

	<span v-for="language in country.languages">
      	{{language}}
     	 </span>

