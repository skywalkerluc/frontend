<template>
  <section>
    <div class="flex">
      <happy-button
        type="danger"
        label="Bem vindo ao berrepí"
      />
      <happy-button
        type="info"
        label="Bem vindo ao berrepí"
      />
      <happy-button
        label="Bem vindo ao berrepí"
      />
    </div>
    <div>
      <happy-card >
        <div slot="box-1">
          <happy-button label="Confirmar"/>
        </div>
        <div slot="box-2">
          <happy-button
            type="danger"
            label="Cancelar"
          />
        </div>
      </happy-card>
    </div>
  </section>
</template>

<script>
import HappyButton from '../../components/HappyButton';
import HappyCard from '../../components/HappyCard';

export default {
  components: {
    HappyButton,
    HappyCard
  }
}
</script>
<style lang="scss" scoped>
section {
  margin: 20px;
  div {
    margin-bottom: 20px;
  }
}
.flex {
  display: flex;

  * {
    margin-right: 5px;
  }
}
</style>


