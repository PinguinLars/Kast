<!--suppress SpellCheckingInspection -->
<script>
  import {onMount} from "svelte";

  let args = new URLSearchParams(window.location.search);
  let username = args.get("name");

  const scrollThreshold = 0.75;

  let introShown = false;
  let introElement;

  let nietShown = false;
  let nietElement;

  let echtShown = false;
  let echtElement;

  let eenShown1 = false;
  let eenElement1;

  let jongenShown = false;
  let jongenElement;

  let meerShown = false;
  let meerElement;

  let maarShown = false;
  let maarElement;

  let juistShown = false;
  let juistElement;

  let eenShown2 = false;
  let eenElement2;

  let meisjeShown = false;
  let meisjeElement;

  //Intro secting
  onMount(() => {
    const observer = new IntersectionObserver(
            ([entry]) => {
              introShown = entry.isIntersecting;
            }, {
              threshold: scrollThreshold,
            },
    );

    if (introElement) {
      observer.observe(introElement);
    }

    return () => {
      if (introElement) {
        observer.unobserve(introElement);
      }
    };
  });

  //Niet
  onMount(() => {
    const observer = new IntersectionObserver(
            ([entry]) => {
              nietShown = entry.isIntersecting;
            }, {
              threshold: scrollThreshold,
            },
    );

    if (nietElement) {
      observer.observe(nietElement);
    }

    return () => {
      if (nietElement) {
        observer.unobserve(nietElement);
      }
    };
  });

  //Echt
  onMount(() => {
    const observer = new IntersectionObserver(
            ([entry]) => {
              echtShown = entry.isIntersecting;
            }, {
              threshold: scrollThreshold,
            },
    );

    if (echtElement) {
      observer.observe(echtElement);
    }

    return () => {
      if (echtElement) {
        observer.unobserve(echtElement);
      }
    };
  });

  //Een [1]
  onMount(() => {
    const observer = new IntersectionObserver(
            ([entry]) => {
              eenShown1 = entry.isIntersecting;
            }, {
              threshold: scrollThreshold,
            },
    );

    if (eenElement1) {
      observer.observe(eenElement1);
    }

    return () => {
      if (eenElement1) {
        observer.unobserve(eenElement1);
      }
    };
  });

  //Jongen
  onMount(() => {
    const observer = new IntersectionObserver(
            ([entry]) => {
              jongenShown = entry.isIntersecting;
            }, {
              threshold: scrollThreshold,
            },
    );

    if (jongenElement) {
      observer.observe(jongenElement);
    }

    return () => {
      if (jongenElement) {
        observer.unobserve(jongenElement);
      }
    };
  });

  //Meer
  onMount(() => {
    const observer = new IntersectionObserver(
            ([entry]) => {
              meerShown = entry.isIntersecting;
            }, {
              threshold: scrollThreshold,
            },
    );

    if (meerElement) {
      observer.observe(meerElement);
    }

    return () => {
      if (meerElement) {
        observer.unobserve(meerElement);
      }
    };
  });

  //Maar
  onMount(() => {
    const observer = new IntersectionObserver(
            ([entry]) => {
              maarShown = entry.isIntersecting;
            }, {
              threshold: scrollThreshold,
            },
    );

    if (maarElement) {
      observer.observe(maarElement);
    }

    return () => {
      if (maarElement) {
        observer.unobserve(maarElement);
      }
    };
  });

  //Juist
  onMount(() => {
    const observer = new IntersectionObserver(
            ([entry]) => {
              juistShown = entry.isIntersecting;
            }, {
              threshold: scrollThreshold,
            },
    );

    if (juistElement) {
      observer.observe(juistElement);
    }

    return () => {
      if (juistElement) {
        observer.unobserve(juistElement);
      }
    };
  });

  //Een [1]
  onMount(() => {
    const observer = new IntersectionObserver(
            ([entry]) => {
              eenShown2 = entry.isIntersecting;
            }, {
              threshold: scrollThreshold,
            },
    );

    if (eenElement2) {
      observer.observe(eenElement2);
    }

    return () => {
      if (eenElement2) {
        observer.unobserve(eenElement2);
      }
    };
  });

  //Meisje
  onMount(() => {
    const observer = new IntersectionObserver(
            ([entry]) => {
              meisjeShown = entry.isIntersecting;
            }, {
              threshold: scrollThreshold,
            },
    );

    if (meisjeElement) {
      observer.observe(meisjeElement);
    }

    return () => {
      if (meisjeElement) {
        observer.unobserve(meisjeElement);
      }
    };
  });
  let y;
</script>

<svelte:window bind:scrollY={y}/>

<div bind:this={introElement} class="intro" class:visible={introShown}>
  <div class="heading-one">
    <p>He {username}</p>
  </div>
  <div class="small-text">
    <p>
      Kan je dit alsjeblieft niet doorvertellen, bedankt.
    </p>
  </div>
  <p>
    Dit is best wel moeilijk om te vertellen voor mij, maar ik wil het je toch graag zeggen.
  </p>
  <p>
    Ik voel me:
  </p>
</div>

<div bind:this={nietElement} class="niet text-box" class:visible={nietShown}>
  <p><b>niet</b></p>
</div>

<div bind:this={echtElement} class="echt text-box" class:visible={echtShown}>
  <p><b>echt</b></p>
</div>

<div bind:this={eenElement1} class="een1 text-box" class:visible={eenShown1}>
  <p><b>een</b></p>
</div>

<div bind:this={jongenElement} class="jongen text-box" class:trans-flag-no-pink-visible={jongenShown}>
  <p><b>jongen</b></p>
</div>

<div bind:this={meerElement} class="meer text-box" class:trans-flag-no-pink-visible={meerShown}>
  <p><b>meer,</b></p>
</div>

<div bind:this={maarElement} class="maar text-box" class:trans-flag-no-pink-visible={maarShown}>
  <p><b>maar</b></p>
</div>

<div bind:this={juistElement} class="juist text-box" class:trans-flag-no-pink-visible={juistShown}>
  <p><b>juist</b></p>
</div>

<div bind:this={eenElement2} class="een2 text-box" class:trans-flag-no-pink-visible={eenShown2}>
  <p><b>een</b></p>
</div>

<div bind:this={meisjeElement} class="meisje text-box trans-flag-visible" class:trans-flag-visible={meisjeShown}>
  <p><b>meisje</b></p>
</div>
