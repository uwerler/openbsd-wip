# $OpenBSD$

COMMENT =	Double Ratchet cryptographic ratchet in C++
V =		3.1.4
DISTNAME =	olm-${V}
CATEGORIES =	devel security

SHARED_LIBS +=	olm       0.0 # 0.0

MASTER_SITES =	https://gitlab.matrix.org/matrix-org/olm/-/archive/${V}/

HOMEPAGE =	https://git.matrix.org/git/olm

MAINTAINER =	Aaron Bieber <abieber@openbsd.org>

# Apache 2.0
PERMIT_PACKAGE =	Yes

WANTLIB += ${COMPILER_LIBCXX} m

MODULES =	devel/cmake
USE_GMAKE =	Yes

COMPILER =	base-clang ports-gcc

MAKE_FLAGS =	CXX="${CXX}" CXXFLAGS="${CXXFLAGS}"

do-test:
	cd ${WRKSRC} && \
		${MAKE_FLAGS} ${MAKE_PROGRAM} test

.include <bsd.port.mk>
