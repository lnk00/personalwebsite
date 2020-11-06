<style type="text/scss">
@import '../../public/assets/theme.scss';

.footer {
  background-color: $dark;
  width: 100%;

  .container {
    justify-content: flex-start;
    display: flex;
    align-items: center;
    max-width: 1280px;
    margin: auto;
    padding: 96px 48px 96px 48px;

    @media (max-width: 480px) {
      padding: 96px 12px 96px 12px;
    }
  }

  .bottom-row {
    color: $white;
    display: flex;
    font-size: 22px;
    width: 100%;
    align-items: baseline;

    @media (max-width: 620px) {
      flex-direction: column;
    }

    .names {
      @media (max-width: 620px) {
        margin-bottom: 12px;
      }

      .firstname {
        margin-right: 12px;
        display: inline-block;
      }

      .lastname {
        font-weight: 900;
        margin-right: 24px;
        display: inline-block;
      }
    }

    .license {
      color: $dark-grey;
      font-size: 14px;
      margin-right: auto;

      @media (max-width: 620px) {
        margin-bottom: 12px;
      }
    }

    .social {
      .fab {
        cursor: pointer;
        font-size: 24px;
        color: $dark-grey;
        margin-left: 12px;
        transition: all 0.3s;

        &:first-child {
          margin-left: 0;
        }

        &:hover {
          color: $green;
        }
      }
    }
  }
}
</style>

<script>
</script>

<div class="footer">
  <div class="container">
    <div class="bottom-row">
      <div class="names">
        <div class="firstname">Damien</div>
        <div class="lastname">Dumontet</div>
      </div>
      <div class="license">© 2020. All Rights Reserved</div>
      <div class="social">
        <a href="https://www.linkedin.com/in/damien-dumontet-5754321aa">
          <i class="fab fa-linkedin"></i>
        </a>
        <a href="https://github.com/lnk00">
          <i class="fab fa-github-square"></i>
        </a>
        <a href="https://www.instagram.com/lnk.0/">
          <i class="fab fa-instagram-square"></i>
        </a>
      </div>
    </div>
  </div>
</div>
