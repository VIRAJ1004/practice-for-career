pipeline{
			agent any
						stages{
								stage('one')
									{
										steps{
												echo 'Hi This is viraj from Tech mahindra'
											 }
									}
								stage('two')
								    {
										steps{
												input('do you want to proceee?')
											 }
									}
								stage('three')
								    {
										steps{
												when{
															not	{
																	branch "master"
																}
													}
											  }
										steps{
												echo "Hello"
											 }
						
									}
								stage('four')
									{
										parallel{
													stage('Unit test')
													{
														steps{
																echo "running Unit test"
															 }
												    }
													stage('integration test')
													{
														agent{ 
																docker 
																		{
																			resuseNode false
																			image 'ubuntu'
													
																		}
															 
											 
																steps{
																					echo "running integaration test"
																	 }
															}		 
														}		 
												}
									}		
			}
		}			
													
													
	}					