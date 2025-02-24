# Feed Page

<div id="query-parameters">
    <!-- 쿼리 파라미터가 여기에 표시됩니다. -->
</div>

<script>
    // 쿼리 파라미터 가져오기
    const queryString = window.location.search;
    const urlParams = new URLSearchParams(queryString);

    // 쿼리 파라미터 표시
    const parameterListDiv = document.getElementById('query-parameters');

    if (queryString) {
        urlParams.forEach((value, key) => {
            const parameterDiv = document.createElement('div');
            parameterDiv.textContent = `${key}: ${value}`;
            parameterListDiv.appendChild(parameterDiv);
        });
    } else {
        const parameterDiv = document.createElement('div');
        parameterDiv.textContent = `No query parameters found`;
        parameterListDiv.appendChild(parameterDiv);
    }
</script>

