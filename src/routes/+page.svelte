<script>
  const storeUrl = 'https://smartstore.naver.com/benasis'
  const ytUrl = 'https://www.youtube.com/@cwj-2025'
  // const instagramUrl =
</script>

<svelte:head>
  <title>최원준가구갤러리</title>
  <meta name="description" content="최원준가구갤러리 스마트스토어 링크" />
</svelte:head>

<main class="page linktree">
  <section class="tree-card">
    <div class="avatar" aria-hidden="true">B</div>
    <h1>최원준가구갤러리</h1>
    <p class="handle">@smartstore</p>

    <nav class="link-list">
      <a class="link-btn ssprimary" href={storeUrl} target="_blank" rel="noopener noreferrer">
        네이버 스마트스토어 방문하기
      </a>
      <a class="link-btn ytprimary" href={ytUrl} target="_blank" rel="noopener noreferrer">
        공식 유튜브 방문하기
      </a>
    </nav>
  </section>
</main>

<style>
  .linktree {
    min-height: calc(100vh - 32px);
    margin-bottom: 0;
    align-items: center;
    justify-content: center;
  }

  .tree-card {
    width: 100%;
    max-width: 560px;
    margin: 0 auto;
    padding: clamp(24px, 5vw, 42px);
    border-radius: 32px;
    border: 1px solid var(--color-border-secondary);
    background:
      var(--color-surface-primary);
    box-shadow: 0 24px 44px var(--lvrs-shadow-strong);
    text-align: center;
  }

  .avatar {
    width: 74px;
    height: 74px;
    border-radius: 999px;
    margin: 0 auto 12px;
    display: grid;
    place-items: center;
    font-size: var(--font-header2);
    font-weight: var(--font-weight-bold);
    color: var(--lvrs-accent-white);
    background: linear-gradient(145deg, var(--lvrs-accent-base-teal), var(--lvrs-accent-dim-green-vivid));
  }

  h1 {
    margin: 0;
    color: var(--color-text-primary);
    font-size: var(--font-title2);
    line-height: 1.06;
    font-weight: var(--font-weight-bold);
  }

  .handle {
    margin-top: 6px;
    color: var(--color-text-octonary);
    font-size: var(--font-caption);
    font-weight: var(--font-weight-regular);
  }

  .link-list {
    margin-top: 22px;
    display: grid;
    gap: 12px;
  }

  .link-btn {
    min-height: 56px;
    border-radius: 16px;
    border: 1px solid var(--color-border-primary);
    background: var(--color-surface-secondary);
    color: var(--color-text-primary);
    font-size: var(--font-body);
    font-weight: var(--font-weight-semibold);
    display: grid;
    place-items: center;
    transition:
      transform 140ms ease,
      background-color 140ms ease,
      border-color 140ms ease;
  }

  .link-btn:hover {
    transform: translateY(-1px);
    background: var(--color-surface-tertiary);
  }

  .link-btn.ssprimary {
    color: var(--lvrs-accent-white);
    border-color: var(--lvrs-accent-transparent);
    background: linear-gradient(145deg, var(--lvrs-accent-base-teal), var(--lvrs-accent-dim-green-vivid));
  }

  .link-btn.ssprimary:hover {
    background: linear-gradient(145deg, var(--lvrs-accent-base-teal), var(--lvrs-accent-base-green-vivid));
  }

  .link-btn.ytprimary {
    color: var(--lvrs-accent-white);
    border-color: var(--lvrs-accent-transparent);
    background: linear-gradient(145deg, var( --lvrs-accent-base-red-vivid), var(--lvrs-accent-dim-red));
  }

  .link-btn.ytprimary:hover {
    background: linear-gradient(145deg, var(--lvrs-accent-dim-red), var(--lvrs-accent-base-red-birch));

    .link-btn.ghost {
      cursor: pointer;
    }

    @media (max-width: 640px) {
      h1 {
        font-size: var(--font-title);
      }
    }
  }
</style>
