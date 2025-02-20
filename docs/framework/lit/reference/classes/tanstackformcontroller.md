---
id: TanStackFormController
title: TanStackFormController
---

# Class: TanStackFormController\<TParentData, TFormValidator\>

Defined in: [tanstack-form-controller.ts:81](https://github.com/TanStack/form/blob/main/packages/lit-form/src/tanstack-form-controller.ts#L81)

## Type Parameters

• **TParentData**

• **TFormValidator** *extends* `Validator`\<`TParentData`, `unknown`\> \| `undefined` = `undefined`

## Implements

- `ReactiveController`

## Constructors

### new TanStackFormController()

```ts
new TanStackFormController<TParentData, TFormValidator>(host, config?): TanStackFormController<TParentData, TFormValidator>
```

Defined in: [tanstack-form-controller.ts:93](https://github.com/TanStack/form/blob/main/packages/lit-form/src/tanstack-form-controller.ts#L93)

#### Parameters

##### host

`ReactiveControllerHost`

##### config?

`FormOptions`\<`TParentData`, `TFormValidator`\>

#### Returns

[`TanStackFormController`](tanstackformcontroller.md)\<`TParentData`, `TFormValidator`\>

## Properties

### api

```ts
api: FormApi<TParentData, TFormValidator>;
```

Defined in: [tanstack-form-controller.ts:91](https://github.com/TanStack/form/blob/main/packages/lit-form/src/tanstack-form-controller.ts#L91)

## Methods

### field()

```ts
field<TName, TFieldValidator, TData>(fieldConfig, render): object
```

Defined in: [tanstack-form-controller.ts:112](https://github.com/TanStack/form/blob/main/packages/lit-form/src/tanstack-form-controller.ts#L112)

#### Type Parameters

• **TName** *extends* `string` \| `number`

• **TFieldValidator** *extends* 
  \| `undefined`
  \| `Validator`\<`DeepValue`\<`TParentData`, `TName`, `IsNullable`\<`TParentData`\>\>, `unknown`\> = `undefined`

• **TData** = `DeepValue`\<`TParentData`, `TName`, `IsNullable`\<`TParentData`\>\>

#### Parameters

##### fieldConfig

`FieldOptions`\<`TParentData`, `TName`, `TFieldValidator`, `TFormValidator`, `TData`\>

##### render

`renderCallback`\<`TParentData`, `TName`, `TFieldValidator`, `TFormValidator`, `TData`\>

#### Returns

`object`

##### values

```ts
values: object;
```

###### values.form

```ts
form: FormApi<TParentData, TFormValidator>;
```

###### values.options

```ts
options: FieldOptions<TParentData, TName, TFieldValidator, TFormValidator, TData>;
```

###### values.render

```ts
render: renderCallback<TParentData, TName, TFieldValidator, TFormValidator, TData>;
```

***

### hostConnected()

```ts
hostConnected(): void
```

Defined in: [tanstack-form-controller.ts:102](https://github.com/TanStack/form/blob/main/packages/lit-form/src/tanstack-form-controller.ts#L102)

Called when the host is connected to the component tree. For custom
element hosts, this corresponds to the `connectedCallback()` lifecycle,
which is only called when the component is connected to the document.

#### Returns

`void`

#### Implementation of

```ts
ReactiveController.hostConnected
```

***

### hostDisconnected()

```ts
hostDisconnected(): void
```

Defined in: [tanstack-form-controller.ts:108](https://github.com/TanStack/form/blob/main/packages/lit-form/src/tanstack-form-controller.ts#L108)

Called when the host is disconnected from the component tree. For custom
element hosts, this corresponds to the `disconnectedCallback()` lifecycle,
which is called the host or an ancestor component is disconnected from the
document.

#### Returns

`void`

#### Implementation of

```ts
ReactiveController.hostDisconnected
```
