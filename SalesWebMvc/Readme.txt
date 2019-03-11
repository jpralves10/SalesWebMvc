*** .Net Core Mvc / MySql ***

1 - Gerar Mvc
	>> (btn direito) Controllers/Adicionar/Novo item com scaffold
	>> Selecionar: Controlador Mvc .. utilizando Entity Framework

2 - Em Startup:
	>> services.AddDbContext<SalesWebMvcContext>(options =>
			options.UseMySql(Configuration.GetConnectionString("SalesWebMvcContext"), builder =>
			builder.MigrationsAssembly("SalesWebMvc")));

3 - Instalar Driver:
	>> Pamelo.EntityFrameworkCore.MySql

4 - Gerar Migration (Via Prompt - Gera o Database):
	>> Add-Migration Initial
	>> Update-Database
