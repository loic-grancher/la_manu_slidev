---
layout : two-cols


---
### Formulaires

<br/>

1) Composant "input/select/..." réutilisables
2) React Hook Form :
    - Gestion des états (state) et erreurs simplifiée
    - Validation intégrée
    - Outils supplémentaires (composant debuggage...)
<br/>

::right::


```tsx
export default function PopupformNotification({ onNotificationCreated }) {
  
  const {
    register,
    handleSubmit,
    watch,
    formState: { errors },
  } = useForm({
    resolver: zodResolver(popupNotificationSchema),
  });

  const selectedStartDate = watch("startDate");

  async function onSubmit(data) {
  ... //manage submission
  }

  return (
    <div >
      <form action="" onSubmit={handleSubmit(onSubmit)}>
        
          <InputText
            label="Titre"
            placeholder="Titre de la notification"
            {...register("title")}
            error={errors.title?.message}
          />

         ...

        <div className={styles.popupButtons}>
          <button className="btn btn-primary"> Créer </button>
        </div>
      </form>
    </div>
  );
}
```


