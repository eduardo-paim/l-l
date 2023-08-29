# Modalizar

[![versão npm](https://badge.fury.io/js/react-native-modalize.svg)](https://badge.fury.io/js/react-native-modalize)

Uma planilha modal/inferior altamente personalizável que adora rolar o conteúdo.

Este componente foi construído com `react-native-gesture-handler` para resolver o problema comum de **rolar**, **deslizar** e lidar com os comportamentos do **teclado**, que você pode enfrentar com o modal do react-native .

Este componente vem com um ScrollView, o renderizador padrão, um FlatList ou um SectionList. Eles são todos integrados e facilitam sua vida, basta passar seu conteúdo e Modalize cuidará do resto para você. Você também pode ter a possibilidade de passar seu próprio renderizador personalizado.

<p align="left">
  <img src="https://user-images.githubusercontent.com/937328/80501705-458d2d80-895f-11ea-9667-d193c135cabf.gif" height="542" alt="Simple" />
  <img src="https://user-images.githubusercontent.com/937328/80501698-42923d00-895f-11ea-8db0-da3d4f772710.gif" height="542" alt="Fixed" />
  <img src="https://user-images.githubusercontent.com/937328/80501699-432ad380-895f-11ea-9dad-22505038234e.gif" height="542" alt="Snapping" />
  <img src="https://user-images.githubusercontent.com/937328/80501647-35754e00-895f-11ea-8ce0-cb53d2985787.gif" height="542" alt="Absolute" />
  <img src="https://user-images.githubusercontent.com/937328/80501682-3efeb600-895f-11ea-9c04-64154cf77012.gif" height="542" alt="FlatList" />
  <img src="https://user-images.githubusercontent.com/937328/80501668-3a3a0200-895f-11ea-92b6-a7bc9b301a1a.gif" height="542" alt="Open" />
  <img src="https://user-images.githubusercontent.com/937328/80615701-881e3b00-8a2f-11ea-94f5-a4cbf6d13d97.gif" height="542" alt="Apple" />
  <img src="https://user-images.githubusercontent.com/937328/80501688-40c87980-895f-11ea-97db-63b9b029eab4.gif" height="542" alt="Facebook" />
  <img src="https://user-images.githubusercontent.com/937328/80501707-4625c400-895f-11ea-8436-8e89de3b437e.gif" height="542" alt="Slack" />
</p>

## Instalação

```bash
fio adicionar react-native-modalize react-native-gesture-handler
```

<detalhes>
   <summary>iOS</summary>

```bash
npx pod-install ios
```

</detalhes>

<detalhes>
   <summary>Android</summary>

#### Reagir nativo <= 0,59

Siga [este guia](https://jeremybarbet.github.io/react-native-modalize/#/INSTALLATION) para concluir a instalação do Android.

#### Reagir nativo > 0,60

Você não precisa seguir o guia mencionado acima porque o link automático do React já executou as etapas.

</detalhes>

## Uso

Aqui está um exemplo rápido, usando o renderizador ScrollView padrão.

```tsx
importar React, {useRef} de 'react';
importar {Visualizar, Texto, TouchableOpacity} de 'react-native';
importar {Modalizar} de 'react-native-modalize';

exportar aplicativo const = () => {
   const modalizeRef = useRef<Modalize>(null);

   const onOpen = () => {
     modalizeRef.current?.open();
   };

   retornar (
     <>
       <TouchableOpacity onPress={onOpen}>
         <Text>Abra o modal</Text>
       </TouchableOpacity>

       <Modalize ref={modalizeRef}>...seu conteúdo</Modalize>
     </>
   );
};
```

## Documentação

Confira a [documentação disponível aqui](https://jeremybarbet.github.io/react-native-modalize) completa para saber tudo sobre os adereços, métodos e exemplos de uso do Modalize.
