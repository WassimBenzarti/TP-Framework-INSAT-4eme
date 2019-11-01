# Part 2: Routing

If there is a service provided in the component level it will persist (doesn't create a new service instance)
this.router.navigate(path, {queryParams:{}});

We need to unsubscribe in the method ngOnDestroy

```typescript
const routes: Routes = [
  {
    path: "todo", component: TodoWrapperComponent, children: [
      { path: ":id", component: TodoDetailComponent },
    ]
  },
  { path: "cv", component: CvViewerComponent },
  { path: "**", component: ComponentError },
];

```

Special path: `path="**"` -> accepts any route (fallback route)