# Protobuf2TypeScript

A script which help front-end devloper to convert *.protobuf file into *.d.ts file.

## Installtion Link

[https://www.raycast.com/gustudio/protobuf2typescript](https://www.raycast.com/gustudio/protobuf2typescript)

## Screenshots

![protobuf2typescript-1](https://github.com/raycast/extensions/assets/8674852/2c08d5f3-fbba-4801-ae3c-5a41fe60863e)
![protobuf2typescript-2](https://github.com/raycast/extensions/assets/8674852/9ba4e4b1-1525-41fd-a786-f2e0cd941819)
![protobuf2typescript-3](https://github.com/raycast/extensions/assets/8674852/d0fed953-1a92-421e-8715-d710bce74a4c)

## Example

Convert this:

```proto
message Person {
  string name = 1;
  int32 id = 2;
  bool isFriend = 3;
  repeated PhoneNumber phones = 4;
}

message PhoneNumber {
  string number = 1;
  PhoneType type = 2;
}

message AddressBook {
  repeated Person people = 1;
}
```

into this:

```typescript
interface Person {
  name: string;
  id: number;
  isFriend: boolean;
  phones: PhoneNumber[];
}

interface PhoneNumber {
  number: string;
  type: PhoneType;
}

interface AddressBook {
  people: Person[];
}
```

## Idea From

- [protobuf-to-typescript ](https://github.com/geotho/protobuf-to-typescript/tree/master)
