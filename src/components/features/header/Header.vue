<script setup>
import Hamburger from '../../icons/Hamburger.vue';
import IconApp from '../../icons/IconApp.vue';
import InputSearch from '../input-search/InputSearch.vue';
import InputSettings from '../../icons/IconSettings.vue';
import IconCampain from '../../icons/IconCampain.vue';
import IconChat from '../../icons/IconChat.vue';
import IconGift from '../../icons/IconGift.vue';
import IconChevron from '../../icons/IconChevron.vue';

</script>
<template>
  <header class="header">
    <div class="container">
      <div class="content-header">
        <div class="navigator">
          <button>
            <Hamburger />
          </button>
          <a href="" class="icon-app">
            <IconApp />
          </a>
        </div>
        <div class="center-menu">
          <div class="searcher">
            <InputSearch />
            <button class="btn-icon bg-green">
              <InputSettings />
            </button>
          </div>
          <div class="notifications">
            <button class="btn-icon bg-gray campain-button">
              <IconCampain />
              <span class="badge-yellow"></span>
            </button>
            <button class="btn-icon bg-gray chat">
              <IconChat />
              <span class="badge-yellow"></span>
            </button>
            <button class="btn-icon bg-gray gift">
              <IconGift />
              <span class="badge-gray"></span>
            </button>
          </div>
        </div>
        

        <div class="nav-config">
          
          <div class="account">
            <button class="btn-icon bg-gray-light">
            </button>
            <div class="text">
              <p>David</p>
            </div>
            <div class="dropwdown">
              <IconChevron />
            </div>
          </div>
        </div> 
      </div>
    </div>
  </header>
</template>

<style lang="scss">
  @import '../../../assets/modules/mixins';

  .header {
    font-size: 16px;

    @include media('mobile') {
      font-size: 10.5px;
    }
  }
  .content-header {
    display: flex;
    justify-content: space-between;
    padding: 2em 0;
  }

  .navigator {
    display: flex;
    gap: 1em;
    margin-right: 6.9em;

    .icon-app {
      svg {
        width: 5.3em !important;
      }
    }
    @include media('mobile') {
      margin-right: 3.9em;
    }

    button {
      background: transparent;
      border: none;
    }
  }

  
  .center-menu {
    display: flex;
    gap: 17.5em;
    flex: 1;

    @include media('mobile') {
      justify-content: flex-end;
      align-items:center;
    }

    .searcher {
      display: flex;
      gap: 1.25em;
      flex: 1;

      @include media('mobile') {
        display: none;
      }
    }
    .notifications {
      display: flex;
      gap: 1.5em;

      @include media('mobile') {
        .gift,
        .chat {
          display: none;
        }
      }

      .campain-button {
        svg {
          width: 1.5em !important;
          height:  1.5em !important;
        }
      }
    }

    
  }
  .nav-config {
    display: flex;
    
    margin-left: 4.5em;

    @include media('mobile') {
      margin-left: 1em;
    }

    color: #fff;
    
    .account {
      display: flex;
      align-items: center;
      gap: 1.5em;
      border-radius: 12px;
      border: 0.5px solid rgba(238, 255, 243, 0.04);

      .text {
        @include media('mobile') {
          display: none;
        }
      }
    }
  }
</style>