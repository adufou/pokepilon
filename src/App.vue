<script setup lang="ts">
import { Tabs, TabsList, TabsTrigger, TabsContent } from '@/components/ui/tabs'
import MapPage from '@/components/MapPage.vue'
import LinksPage from '@/components/LinksPage.vue'
import DonateButton from '@/components/DonateButton.vue'
</script>

<template>
  <Tabs default-value="map" class="h-screen flex flex-col overflow-hidden">
    <header class="flex items-center justify-between px-6 py-3 border-b border-border">
      <div class="flex items-center gap-4">
        <span class="font-semibold text-lg">PokéPilon</span>
        <span class="text-sm text-muted-foreground">IP : pokepilon.location-minecraft.fr</span>
      </div>
      <TabsList>
        <TabsTrigger value="map">Map</TabsTrigger>
        <TabsTrigger value="links">Liens Utiles</TabsTrigger>
      </TabsList>
      <DonateButton />
    </header>
    <main class="flex-1 flex flex-col">
      <TabsContent value="map"><MapPage /></TabsContent>
      <TabsContent value="links"><LinksPage /></TabsContent>
    </main>
  </Tabs>
</template>

<style scoped></style>
