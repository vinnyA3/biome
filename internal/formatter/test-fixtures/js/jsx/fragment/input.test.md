# `index.test.ts`

**DO NOT MODIFY**. This file has been autogenerated. Run `rome test internal/formatter/index.test.ts --update-snapshots` to update.

## `js > jsx > fragment`

### `Diagnostics`

```
✔ No known problems!

```

### `Input`

```js
function Component() {
	return (<></>);
}

function Component1() {
	return (<>Lorem ipsum</>);
}

function Component2() {
	return <>
		<Foo />
		<Foo />
	</>;
}

function Component2() {
	return <>
		<>
			<></>
		</>
	</>;
}

```

### `Output`

```js
function Component() {
	return <></>;
}

function Component1() {
	return <>
		Lorem ipsum
	</>;
}

function Component2() {
	return <>
		<Foo />
		<Foo />
	</>;
}

function Component2() {
	return <>
		<>
			<></>
		</>
	</>;
}

```