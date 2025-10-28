# test-sync
Testing sync - 4

export const useUpdateOrchestratorModel = (shouldInvalidate: boolean = false) => {
	const queryClient = useQueryClient();
	const queryParameters = new URLSearchParams(window.location.search);
	const taskId = queryParameters.get('taskId');
	return useMutation({
		mutationFn: async ({ task_id, model_data }: { task_id: string; model_data: InferenceModelConfig }) => {
			return updateOrchestratorModel(task_id, model_data);
		},
		onSuccess: async () => {
			await queryClient.invalidateQueries({ queryKey: ['PROJECT-INGESATION', 'GET-SUMMARY', taskId] });
		},
		onError: (error) => {
			console.error('Error updating model:', error);
		}
	});
};
export const useUpdateOrchestratorModel = (shouldInvalidate: boolean = false) => {
	const queryClient = useQueryClient();
	const queryParameters = new URLSearchParams(window.location.search);
	const taskId = queryParameters.get('taskId');
	return useMutation({
		mutationFn: async ({ task_id, model_data }: { task_id: string; model_data: InferenceModelConfig }) => {
			return updateOrchestratorModel(task_id, model_data);
		},
		onSuccess: async () => {
			await queryClient.invalidateQueries({ queryKey: ['PROJECT-INGESATION', 'GET-SUMMARY', taskId] });
		},
		onError: (error) => {
			console.error('Error updating model:', error);
		}
	});
};
export const useUpdateOrchestratorModel = (shouldInvalidate: boolean = false) => {
	const queryClient = useQueryClient();
	const queryParameters = new URLSearchParams(window.location.search);
	const taskId = queryParameters.get('taskId');
	return useMutation({
		mutationFn: async ({ task_id, model_data }: { task_id: string; model_data: InferenceModelConfig }) => {
			return updateOrchestratorModel(task_id, model_data);
		},
		onSuccess: async () => {
			await queryClient.invalidateQueries({ queryKey: ['PROJECT-INGESATION', 'GET-SUMMARY', taskId] });
		},
		onError: (error) => {
			console.error('Error updating model:', error);
		}
	});
};
