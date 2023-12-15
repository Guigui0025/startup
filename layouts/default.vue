<template>
  <Head>
    <Title>RecyCraft</Title>
    <Meta name="description" content="Design System" />
  </Head>
  <LayoutsBase>
    <template #navigation>
      <NavsNav>
        <template #logo>
          <TitresLogo>RecyCraft</TitresLogo>
        </template>

        <template #links>
          <LinksNavLink to="/">Accueil</LinksNavLink>
          <LinksNavLink to="/produits">Produits</LinksNavLink>
          <LinksNavLink to="/societe">Société</LinksNavLink>
          <LinksNavLink to="/equipe">Équipe</LinksNavLink>
          <LinksNavLink to="/contact">Contact</LinksNavLink>
          <LinksNavLink to="/blog">Blog</LinksNavLink>
        </template>
      </NavsNav>
    </template>

    <template #content>
      <slot />
    </template>

    <template #footer>
      <FootersBasic />
    </template>
  </LayoutsBase>
</template>
