# hvScriptSet

## Version: 1.0.15

### Author: Человек-Шаман

### License: MIT

### Description

hvScriptSet is a script for modifying user profile masks within a single message. It is designed for the MyBB platform and offers a variety of customization options for user profiles within posts.

### Features

- Store up to 20 masks by default (configurable).
- Supports HTML, BBCode, and text modifications.
- Dynamic preview of mask changes.
- Easy installation and configuration.
- Compatibility with custom fields and extended access controls.

### How to Install

1. Configure the script for your forum. Choose which sections, users, and what can be modified. Administrators and Moderators have full access by default.
2. Add the option to change additional profile fields.
3. Generate the script code at the bottom of the settings page.
4. Insert the generated code into the HTML footer in the "Administration » Settings" section of your forum.
5. Test the script from a user account. Note that administrators and moderators have full access by default.

### How to Use

1. Find the mask dialog button above the reply form.
2. Follow the prompts in the dialog window. The mask preview updates automatically when profile fields lose focus.
3. The right side of the dialog shows previously used masks. You can reuse them by clicking on the avatar thumbnail or delete them from this list (deletion is irreversible).

### Troubleshooting

For support, contact the script author at [homoveneficus@gmail.com](mailto:homoveneficus@gmail.com) or on the MyBB support forum: [http://forum.mybb.ru/](http://forum.mybb.ru/)

### Configuration Options

```javascript
const options = {
  changeList: {
    'characterName': {
      title: 'Имя персонажа',
      description: 'Только текст',
      tag: 'charname',
      class: 'pa-character-name',
      type: 'text'
    },
    'raceAndAge': {
      title: 'Раса и возраст',
      description: 'Только текст',
      tag: 'raceage',
      class: 'pa-race-age',
      type: 'text'
    },
    'status': {
      title: 'Статус',
      description: 'Должность, род деятельности, принадлежность, покровительство, имущество',
      tag: 'status',
      class: 'pa-status',
      type: 'text'
    },
    'appearance': {
      title: 'Внешность',
      description: 'Рост, телосложение, цвет волос, цвет глаз, описание, прототип, истинный облик',
      tag: 'appearance',
      class: 'pa-appearance',
      type: 'text'
    },
    'character': {
      title: 'Характер',
      description: 'Только текст',
      tag: 'character',
      class: 'pa-character',
      type: 'text'
    },
    'preferences': {
      title: 'Предпочтения',
      description: 'Только текст',
      tag: 'preferences',
      class: 'pa-preferences',
      type: 'text'
    },
    'abilities': {
      title: 'Способности',
      description: 'Навыки, увлечения, магические способности, магические слабости',
      tag: 'abilities',
      class: 'pa-abilities',
      type: 'text'
    },
    'magicItems': {
      title: 'Магические предметы',
      description: 'Только текст',
      tag: 'magicitems',
      class: 'pa-magic-items',
      type: 'text'
    },
    'biography': {
      title: 'Биография',
      description: 'Только текст',
      tag: 'biography',
      class: 'pa-biography',
      type: 'text'
    },
    'contact': {
      title: 'Связь и частота посещения',
      description: 'Только текст',
      tag: 'contact',
      class: 'pa-contact',
      type: 'text'
    },
    'samplePost': {
      title: 'Пробный пост',
      description: 'Только текст',
      tag: 'samplepost',
      class: 'pa-sample-post',
      type: 'text'
    }
  },
  userFields: ['pa-character-name', 'pa-race-age', 'pa-status', 'pa-appearance', 'pa-character', 'pa-preferences', 'pa-abilities', 'pa-magic-items', 'pa-biography', 'pa-contact', 'pa-sample-post'],
  defaultAvatar: 'https://i.imgur.com/bQuC3S1.png',
  maskLimit: 20,
  showPreview: true,
  buttonImage: 'https://i.imgur.com/ONu0llO.png'
};
