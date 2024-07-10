- [x] check the new localization service ✅ 2024-06-24
- [ ] check new `editableTranslations` and `translationTitle` fields in the `data` fields of the routes
- [x] remove `errorMessagesDict`, `descriptionErrorDict`, `errorsDict` ✅ 2024-06-18
- [x] check the `app-input` component and its usage ✅ 2024-06-24
- [x] `error-renderer-control-wrapper` is being changed to `form-control-wrapper` in `scss` ✅ 2024-06-18
- [x] the following translation code block is being removed across the application ✅ 2024-06-24
```typescript
this.translateService  
  .stream('errors.required')  
  .pipe(takeUntil(this.unsubscribe$))  
  .subscribe((translate) => {  
    this.errorsDict = {  
      required: translate  
    };  
  });
```
- [x] use `appBaseRevisionMask` on items' numbers and revisions ✅ 2024-06-24
- [x] `validationErrorService.showFormValidation` is replaced by `validationErrorService.validateControls()` ✅ 2024-06-24
- [ ] 