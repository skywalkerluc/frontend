<template>
  <section>
    <happy-topbar/>
    <div class="content">
      <p class="label">Botões</p>
      <div class="flex">
        <happy-button
          type="danger"
          label="Danger Button"
        />
        <happy-button
          type="info"
          label="Info Button"
        />
        <happy-button
          type="primary"
          label="Primary Button"
        />
        <happy-button
          label="Normal Button"
        />
        <happy-button
          disabled
          label="Disabled Button"
        />
      </div>
      <p class="label">Cards</p>
      <div>
        <happy-card
          title="Titulo do card"
          resume="ewhqoiuewhoiuwehouiqwehqowuiehqweouihweouihqew"
          image="https://is3-ssl.mzstatic.com/image/thumb/Purple19/v4/44/d5/52/44d552f0-9ade-4714-652e-c0a9a6ef2ad7/pr_source.png/246x0w.jpg">
          <happy-button
            slot="footer"
            type="danger"
            label="Bem vindo ao Birrépi! =)"
          />
        </happy-card>
      </div>
      <div style="display: flex; flex-wrap: wrap;">
        <div style="max-width: 50%; width: 50%;">
          <happy-card
            style="margin-right: 10px;"
            title="Titulo do card"
            resume="50% card size"/>
        </div>
        <div style="max-width: 50%; width: 50%;">
          <happy-card
            title="Titulo do card"
            resume="50% card size"/>
        </div>
        <div style="max-width: 50%; width: 50%;">
          <happy-card
            title="Titulo do card"
            resume="50% card size"/>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import HappyButton from '../../components/HappyButton';
import HappyCard from '../../components/HappyCard';
import HappyTopbar from '../../components/HappyTopbar';

export default {
  components: {
    HappyButton,
    HappyCard,
    HappyTopbar,
  }
}
</script>
<style lang="scss" scoped>
section {
  div {
    margin-bottom: 20px;
  }

  .content {
    margin: 20px;
  }
}
.label {
  font-weight: 600;
  font-size: 1.2em;
  margin: 30px 0px;
  border-bottom: 1px solid rgba(0,0,0,0.15);
}
.flex {
  display: flex;
  flex-wrap: wrap;

  *:not(:last-child) {
    margin-right: 20px;
    margin-bottom: 20px;
  }
}
</style>


