```js
// La liste des rangées de la grille
  const [rows, setRows] = useState([]); 
//Ce state est modifié lorsque les données sont récupérées au chargement du composant

const colDefs = [
    { field: "Nom Prénom", filter: true },
    ...
    {
      field: "Actions",
      filter: false,
      actions: [
        {
          label: "Pdf",
          onClick: (data) => exportToPdf(data),
          icon: {
            icon: "material-symbols:visibility",
          },
        },
      ],
    },
  ];
  
  ...
  
 <DataGrid pageSize={pageSize} colDefs={colDefs} rowData={rows} />
 ```
