# Technikus

# NuGets:
 - Microsoft.EntityFrameworkCore (8.0.23)
 - Microsoft.EntityFrameworkCore.Design (8.0.23)
 - Microsoft.EntityFrameworkCore.Tools (8.0.23)
 - Microsoft.EntityFrameworkCore.Sqlite (8.0.23)

#Context osztály létrehozása:

public class DatabaseContext : DbContext
{
  public DatabaseContext(DbContextOptions<DatabaseContext> options) : base(options) {}

  public DbSet<Model> Models {get;set;}
}

#Appsettings.json: 
"ConnectionStrings": {
  "DatabaseContext": "Data Source=SQLiteDatabaseContext.db"
}

#Program.cs:
builder.Services.AddDbContext<PoolCarContext>(  
  db => db.UseSqlite(builder.Configuration.GetConnectionString("PoolCarContext"))); 

 
