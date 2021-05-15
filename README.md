# go-graphql

## RUN serve

```
go run server.go
```

### SOME GQL EXAMPLES:

```
mutation createCategory {
  createCategory(input: { name: "GO", description: "GO is awesome" }) {
    id
    name
    description
  }
}

mutation createCourse {
  createCourse(input: { name: "Evolving with GO", description: "GQL in GOlang is awesome", categoryId: "T5577006791947779410" }) {
    id
    name
    description
    category {
      id
      name
    }
  }
}

mutation createChapter {
  createChapter(input: { name: "GO basics", description: "GO operators", courseId: "T8674665223082153551" }) {
    id
    name
    course {
      id
      name
    }
  }
}

query findCategories {
  categories {
    id
    name
    description
    courses {
      id
      name
      description
      chapters {
        id
        name
      }
    }
  }
}

query findCourses {
  courses {
    id
    name
    description
    chapters {
      id
      name
    }
  }
}

query findChapters {
  chapters {
    id
    name
  }
}
```
