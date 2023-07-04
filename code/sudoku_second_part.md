
int main()
{
	memset(row, 0, sizeof(row));
	memset(column, 0, sizeof(column));
	memset(grid, 0, sizeof(grid));
	for(int i=1; i<=9; ++i){
		for(int j=1; j<=9; ++j){
			cin >> a[i][j];
			if(a[i][j]){
				int num=a[i][j];
				
				int grid_num=(i-1)/3*3+ceil(j/3.0);
				
				row[i][num]=true;
			
				column[j][num]=true;
				
				grid[grid_num][num]=true;
			}
		}
	}
	for(int i=1; i<=37; ++i){
		printf("-");
	}
	printf("\n");
	
	dfs(1, 1);
	return 0;
}

