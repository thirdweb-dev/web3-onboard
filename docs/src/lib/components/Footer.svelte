<script>
  import Flexbox from './base/Flexbox.svelte'
  import PoweredByTw from './svg/powered-by-thirdweb.svg'

  import DiscordIcon from '~icons/ri/discord-fill'
  import GitHubIcon from '~icons/ri/github-fill'
  import TwitterIcon from '~icons/ri/twitter-fill'
  import YoutubeIcon from '~icons/ri/youtube-fill'

  export let iconSize = 40

  let text = {
    license: 'Released under the MIT License',
    copyright: '© 2025 thirdweb'
  }
</script>

<footer>
  <Flexbox
    --direction="column"
    --justify-content="center"
    --align-items="center"
    --gap="2rem"
    --flex="1"
    --padding="2rem"
  >
    <Flexbox --direction="row" --gap="2rem" --padding="0">
      <a class="icon-link" href="//github.com/thirdweb-dev/web3-onboard" target="_blank">
        <GitHubIcon width={iconSize} height={iconSize} />
        <span class="sr-only">Github</span>
      </a>
      <a class="icon-link" href="//discord.com/invite/thirdweb" target="_blank">
        <DiscordIcon width={iconSize} height={iconSize} />
        <span class="sr-only">Discord</span>
      </a>
      <a class="icon-link" href="https://x.com/thirdweb" target="_blank">
        <TwitterIcon width={iconSize} height={iconSize} />
        <span class="sr-only">X (formerly Twitter)</span>
      </a>
      <a class="icon-link" href="//www.youtube.com/channel/UCdzMx7Zhy5va5End1-XJFbA" target="_blank">
        <YoutubeIcon width={iconSize} height={iconSize} />
        <span class="sr-only">Youtube</span>
      </a>
    </Flexbox>
    <a href="//www.thirdweb.com/" target="_blank" class="logo-link">
      <img src={PoweredByTw} alt="Powered by thirdweb" style="max-height: 20px;" />
      <span class="sr-only">Powered by thirdweb</span>
    </a>
  </Flexbox>
  <div class="copyright-box">
    <div class="flex flex-row flex-wrap justify-center">
      <div class="text">{text.license} {text.copyright}</div>
    </div>
    <div class="flex">
      <a
        target="_blank"
        href="https://thirdweb.com/privacy-policy"
        class="text-sm hover:text-white">Privacy Policy</a
      >
      <div class="w-px bg-gray-divider mx-2 h-4" />
      <a
        target="_blank"
        href="https://thirdweb.com/terms"
        class="text-sm hover:text-white">Terms of Service</a
      >
    </div>
  </div>
</footer>

<style>
  footer {
    background: #ebebed;
    min-height: 200px;
    display: flex;
    flex-flow: column;
  }

  a.icon-link {
    color: rgba(20, 20, 20, 0.8);
    transition: transform 200ms ease-in-out;
  }
  a.icon-link:hover {
    color: rgba(20, 20, 20, 1.0);
    transform: scale(1.1);
  }
  a.icon-link:focus {
    transform: none;
  }

  a.logo-link {
    opacity: 0.8;
  }
  a.logo-link:hover {
    opacity: 1.0;
  }

  .copyright-box {
    /* grey/600 */
    background: #242835;
    display: flex;
    flex-flow: column;
    justify-content: center;
    align-items: center;
    padding: 1.5rem 2rem;
    gap: 1rem;
  }
  @media screen and (min-width: 1024px) {
    .copyright-box {
      flex-flow: row;
      justify-content: space-between;
      gap: 0.5rem;
    }
  }

  .text {
    /* F6 */
    font-family: 'Sofia Pro';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 16px;
    /* grey/300 */
    color: #999ca5;
  }

  /* screen reader class */
  /* can be moved elsewhere */
  .sr-only {
    position: absolute;
    width: 1px;
    height: 1px;
    padding: 0;
    margin: -1px;
    overflow: hidden;
    clip: rect(0, 0, 0, 0);
    white-space: nowrap;
    border-width: 0;
  }
</style>
