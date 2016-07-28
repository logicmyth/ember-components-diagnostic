# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components.

    ```md
Route
Model
Template
Component
Data down actions up
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
ember g component my-map    ```

1.  What files are edited to produce a component, and what are their
    responsibilities?

    ```md
component.js, template.hbs. Component is where the JS goes. Template is where
the handlebars goes for display.    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` path. What is
    the syntax for loading this component inside that template?


    ```
    html
    {{#link-to /contacts/template.hbs}}my-contact{{/link-to}}
    ```

    Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    {{#each components.my-contact as |contact|}}
      {{components/my-contact/my-phone personOnMyPhone=contact}}
    {{/each}}
    ```
